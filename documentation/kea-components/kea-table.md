---
chapter: Kea Components
index: kea-components
icon: "KeaLogo.png"
title: Kea Table
layout: template
filename: kea-table
toc:
    - Getting started
    - Apply styling
    - Emitted events
    - Caption and Footer
    - Column order and column choice
    - Filter
    - Selection
    - Pagination
    - Buttons
    - Sorting
    - Custom cell functions
    - Custom row function
    - Configuration
    - Use with a framework like Vue
--- 

# Kea Table
Kea Table has been designed so that you can use the styling framework or any javascript framework of your choice and still be able to just add this component.

**Features**

* Supports vanilla js or any js framework like Vue
* Supports regular css or any styling framework like Bootstrap
* Sorting: single column or even multiple columns at the same time
* Table wide Filtering, including case sensitive and custom cell outputs
* Pagination
* Column order and column choice
* Custom cell functions
* Custom row function
* Able to add classes
* Lifecycle hooks
* Add caption / footer
* Add buttons
* Able to single and multi-select

# Getting started
Add the .js file to your project and include it to the html file in which you want to use it.
Replace the path to where the file is located and replace X.Y.Z with the version you currently have.

**Example:**
```html
<head>
    <script defer src="/js/kea-table-X.Y.Z.min.js"></script>
</head>
```

Now you can add it to the page like: 

```html
<kea-table id="kea-table"></kea-table>
```

Add the following script:

```html
<body>
    ...
    <script>
    window.onload = () => {
        const tablecontent = {
            headers: {
                ScientificName: 'Scientific name',
                common_name: 'Common name',
            },
            content: [
                        {
                            ScientificName: "Ardea cinerea",
                            common_name: "Grey heron"
                        },
                        {
                            ScientificName: "Ardea herodias",
                            common_name: "Great blue heron"
                        },
                        {
                            ScientificName: "Ardea cocoi",
                            common_name: "Cocoi heron"
                        },
                        {
                            ScientificName: "Ardea pacifica",
                            common_name: "White-necked heron"
                        },
                        {
                            ScientificName: "Ardea melanocephala",
                            common_name: "Black-headed heron"
                        },
                        {
                            ScientificName: "Ardea humbloti",
                            common_name: "Humblot's heron"
                        },
                        {
                            ScientificName: "Ardea insignis",
                            common_name: "White-bellied heron"
                        },
                        {
                            ScientificName: "Ardea sumatrana",
                            common_name: "Great-billed heron"
                        },
                        {
                            ScientificName: "Ardea goliath",
                            common_name: "Goliath heron"
                        },
                        {
                            ScientificName: "Ardea purpurea",
                            common_name: "Purple heron"
                        },
                        {
                            ScientificName: "Ardea alba",
                            common_name: "Great egret, great white heron"
                        },
                        {
                            ScientificName: "Ardea brachyrhyncha",
                            common_name: "Yellow-billed egret"
                        },
                        {
                            ScientificName: "Ardea intermedia",
                            common_name: "Medium egret"
                        },
                        {
                            ScientificName: "Ardea plumifera",
                            common_name: "Plumed egret"
                        }
                    ],
            };
        const tableEl = document.getElementById('kea-table');
        tableEl.Render(tablecontent);
    }
    </script>
</body>
```

<img class="inline-block" src='../images/triangle-alert.png' style="position:relative;top:4px;margin-right:8px;" /> By default, there is no styling applied. The component does **not** use shadow dom, so any styling to regular HTML tables is also applied here.

# Apply styling
You can apply styling within the table object:

```javascript
const tableOptions = {
    headers: { ... },
    content: [ ... ],
    table: {
        classList: [],          /** string[] of classes to apply to <table> element                                     */
        caption: "",            /** html string of what to place in a caption on top.                                   */
        captionClassList: [],   /** string[] of classes to apply to <caption> element                                   */
        footer: "",             /** html string to be placed inside footer                                              */
        footerClassList: "",    /** string[] of classes to apply to <tfoot> element                                     */
        emptyResultsText: ""    /** Text to display when there are no results, for example when filter has no results   */
    }
}
```

You can also directly apply styling to ```<kea-table>```. By default it is rendered as ```display: inline-block;```

# Emitted Events
All events that are emitted by ```<kea-table>```

**loaded**
The event 'loaded' is triggered when the element is added to the DOM. You can listen to this with an eventListener:

```javascript
const tableEl = document.getElementById('kea-table');
tableEl.addEventListener('loaded', () => console.log("Kea Table has been loaded!"));
```

**rendered**
The event 'rendered' is triggered when the element is done drawing itself. You can listen to this with an eventListener:

```javascript
const tableEl = document.getElementById('kea-table');
tableEl.addEventListener('rendered', () => console.log("Kea Table has been fully drawn!"));
```

**filter-results**
When you apply a filter, after filtering is done, this event is emitted.

You get the following signature object within the event:

```javascript
{
    ...
    details: {
                numberOfResults: Number 
             }
    ...
}
```

How to listen to this event:

```javascript
const tableEl = document.getElementById('kea-table');
tableEl.addEventListener('filter-results', (event) => console.log(event.details));
```

**row-select**
Whenever you click a checkbox or a radiobutton, this event is emitted.
If you have a checkbox, you will get an array back, if you have a radiobutton you only get a single id.


```javascript
const obj = {
    ...
    details: {
                selection: string | string[] 
             }
    ...
}
```

How to listen to this event:

```javascript
   const tableEl = document.getElementById('kea-table');
   tableEl.addEventListener('row-select', (event) => console.log(event.details));
```

**custom button event**

```javascript
const obj = {
    innerHTML:"",  // the html to display in the button
    classList: []  // string[] which classes to add to the button
    event: ""      // the name of the event emitted when clicked
    order: number  // the order of which the button appears.
}
```

Whatever event name you put in the object of the button, that will be emitted.
See [buttons](#buttons) section for more details.

# Caption and Footer
You can add a Caption and or a Footer to the table by adding the following entry in the configuration:

```javascript
const tableOptions = {
    headers: {},
    content: [],
    table:  {
                ...
                caption: html string of what to place in a caption on top.
                captionClassList:  string[] of classes to apply to <caption> element
                footer:  html string to be placed inside footer
                footerClassList:  string[] of classes to apply to <tfoot> element
                ...
            }
    ...
}
```

<img class="inline-block" src='../images/triangle-alert.png' style="position:relative;top:4px;margin-right:8px;" /> You do not need to add ```<caption></caption>``` or ```<footer></footer>```  as html. 
The html and classes you provide will be automatically put in the respective element.

# Column order and column choice
The order you put the keys in, is the order how the columns are ordered.

```javascript
const tableOptions = {
    headers: {
        columnB: "This column will be first",
        columnC: "This column will be second",
        columnA: "This column will be third",
    },
    content: [{
      columnA: "A"  
      columnB: "B"  
      columnC: "C"  
      columnD: "D"  
    }]
    ...
}
``` 

Because ```columnD``` was not included in the headers, it will not be shown or rendered.

**Feature**:
You can even add keys to the ```headers``` object that do not exist. This allows you to create custom / computed fields using [Custom cell functions](#custom-cell-functions).

# Filter
If you add the following property to the object, the table will be filtered:

```js
const tableOptions = {
    headers: { ... },
    content: { ... },
    filter: { 
        match: string,               // The string you want to search for.
        caseSensitive: true/false,   // if not provided, defaults to false
        property: ""                 // If provided, will search only in given colum, defaults to all columns
    }
    ...
}
```

# Selection
If you add the following property you automatically add either checkboxes or radiobuttons to the table:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    selectionBar: {
            location: left/right,
            classList: string[]        // which classes to add to the checkbox,
            checkbox: true/false       // Choose either checkbox or radio button
            radiobutton: true/false    // Choose either checkbox or radio button
            selectionProperty: ""      // Key of the object that contains unique value.
        }
    ...
}
```
**location** <br/>
If you want the checkboxes or radiobuttons want to have at the left or right side of the table

**classList** <br/>
If you want to style the checkbox in a certain way, you can add the classes and they will be added to the inputs.

**selectionProperty** <br/>
Which of the values that are inside the objects should be used to emit on selection. Should be unique to identify the correct row.

# Pagination
Add the following property:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    pagination: { 
        page: number, // Not zero-based, so starts at 1
        itemsPerPage: number
    }
    ...
}
```

**page** <br/>
The page you want to show, starting at 1.

**itemsPerPage** <br/>
The amount of items you want to show.

# Buttons
You can add buttons to the table, for example to make a CRUD table for database management.
This is how you do it:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    buttonBar: {
                location: "left"|"right",
                tableRowClassList: []   // string[] which classes to add to the table row, for example to make the buttons only available on hover
                rowIdProperty: ""       // the exact name of the object key that will be emitted when the button is clicked, works the same as 'selection'
                buttonBarClassList: []  // string[] which classes to add to the buttonbar div.
                buttons: [
                            {
                                innerHTML: "",  // the html to display in the button
                                classList: [],  // string[] which classes to add to the button
                                event: "",      // the name of the event emitted when clicked, e.g. "row-edit"
                                order: number   // the order of which the button appears.
                            }
                    ]
               }
    ...
}
```

# Sorting
By default you can click on any header to start sorting the table.
You can also do it by default by adding the following property:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    order: [
            { 
                propertyName: string,       // the object property to sort on
                descending: true/false      // defaults to ascending if not provided
            }
        ]
    ...
}
```

If you have multisort enabled, you can add multiple sorting objects. Else just add only one object to the array.

**Sorting on multiple columns** <br/>
Default it sorts only on a single column. Add ```multiSort``` to true like this:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    multiSort: true
    ...
}
```

<img class="inline-block" src='../images/triangle-alert.png' style="position:relative;top:4px;margin-right:8px;" /> If you have dates that are not the default ```yyyy-mm-dd```, or have different seperators add a description of this to the object like so:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    
    /** example date would be 12-31-2025 */
    contentMetadata: {
                myDateColumn: {
                            type: "date",
                            format: "mmddyyyy",     // can also be single char like dmy,
                            separator: "-"
                    }
            }                         
    ...
}
```

# Custom cell functions
Custom cell functions are a powerful way to customize the table cell output:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },

    /** Object, Key: Value, Key is the exact JSON object key that is also present in the headers object, Value is a function (value, prop, object), must return a string, which will be put in the innerHTML of the td                                */
    cellFunctions: {},         
    ...
}
```

**Function signature** <br/>
You can use ```function() {} or () => {}```, here is an example:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    cellFunctions: {
        "myColumnName": (value, property, object) => {
         ...
        },
    ...
    }
}
```

**value** <br/>
A string that is the original value, if you use a non-existent key, it is empty. 

**property** <br/>
The key of the object that this function belongs to. if you access ```object[property]``` you get the processed value, 
so if you access a property that also has a custom function and you access that from the object, 
you get the processed version. This is due to the fact that the table is pre-processed to enable full filtering.

**object** <br/>
The complete row object, so you can use any values, even the ones you do not have in the ```header```.

# Custom row function
A custom row function allows you to customize the complete row, allowing adding classes to the row and also have full control over all tablecells!


```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },

    /** You get an empty tablerow html element, the columns (property headers) to access the row data */
    rowFunction: (HTMLElement tr, string[] columns, rowObject) => {},         
    ...
}
```

**Function signature** <br/>
You can use ```function() {} or () => {}```, here is an example:

```javascript
const tableOptions = {
    headers: { ... },
    content: { ... },
    rowFunction: (row, columns, object) => {
        ...
    }
}
```

**row** <br/>
A ```<tr></tr>``` element, without any table cells. 

**columns** <br/>
An array of keys of the object that is used for this row. if you access ```object[property]``` you get the processed value, 
so if you access a property that also has a custom function and you access that from the object, 
you get the processed version. This is due to the fact that the table is pre-processed to enable full filtering.

**object** <br/>
The complete row object, so you can use any values, even the ones you do not have in the ```header```.


# Configuration
Complete overview of the options you can pass into the ```Render()``` function:

```javascript
const tableOptions = {
    headers: {},               /** [Required] Object with Key: Value where Key is the exact JSON object key, Value is the displayed text.  */

    content: [],               /** [Required] Array, each object is a row in the table. The Keys corresponds with the header keys.         */

    contentMetadata: {},       /** [Optional] Used for sorting. Object with Key: Value, Key is the exact JSON object key, 
                                *  Value is an Object with type, format and separator (for date), types supported: date 
                                *  example date would be 12-31-2025 
                                *  myDateColumn: {
                                *                  type: "date",
                                *                  format: "mmddyyyy",     // can also be single char like dmy,
                                *                  separator: "-"
                                *                 }
                                */

    buttonBar: {},             /** [Optional] Adds a button bar.
                                *  Object   {
                                *              location: left/right,
                                *              tableRowClassList: string[] which classes to add to the table row, 
                                *              for example to make the buttons only available on hover
                                * 
                                *              rowIdProperty: the exact name of the object key that will be emitted 
                                *              when the button is clicked
                                * 
                                *              buttonBarClassList: string[] which classes to add to the buttonbar div.
                                *              buttons: [
                                *                          {
                                *                              innerHTML: the html to display in the button
                                *                              classList: string[] which classes to add to the button
                                *                              event: the name of the event emitted when clicked
                                *                              order: the order of which the button appears.
                                *                          }
                                *                       ]
                                *           }
                                */
    
    selectionBar: {},          /** [Optional] Adds checkboxes or radiobuttons. I case of checkboxes, 
                                *  there will be also one in the header for 'select all'
                                *  Object   {
                                *              location: left/right,
                                *              classList: string[]        // which classes to add to the checkbox,
                                *              checkbox: true/false       // Choose either checkbox or radio button
                                *              radiobutton: true/false    // Choose either checkbox or radio button
                                *              selectionProperty: ""      // Key of the object that contains unique value.
                                *           }
                                */

    cellFunctions: {},         /** [Optional]
                                *  Object, Key: Value
                                *  Key is the exact JSON object key, Value is a function (value, prop, object), must return a string,
                                *  which will be put in the innerHTML of the td
                                */

    rowFunction: function,      /** [Optional] 
                                 * Function (HTMLElement tr, array<string> columns, row data)
                                 * Can be function() {} or () => {}
                                 * Allows full customization of the row.
                                 */

    sortingFunction: function, /** [Optional]
                                *  Object, Key: Value
                                *  Key is the exact JSON object key, Value is a sorting function 
                                *  params: (jsonArray, sortDetails[{propertyName: string, descending: true/false }], metadata = null), 
                                *  must return a function (a, b) which must return 1, 0 or -1
                                *  By default it can sort a lot of values, for dates you can use the contentMetadata to 
                                *  further enhance sorting.
                                */
    
    table: {},                 /** [Optional]
                                *  Object  {
                                *              classList: string[] of classes to apply to <table> element
                                *              caption: html string of what to place in a caption on top.
                                *              captionClassList:  string[] of classes to apply to <caption> element
                                *              footer:  html string to be placed inside footer
                                *              footerClassList:  string[] of classes to apply to <tfoot> element
                                *              emptyResultsText: Text to display when there are no results, 
                                *              for example when filter has no results
                                *          }
                                */

    order: [],                 /** [Optional]
                                *  Object Array
                                *          [
                                *               { 
                                *                  propertyName: string, 
                                *                  descending: true/false
                                *               }
                                *          ] 
                                */   

    multiSort: true/false,     /** [Optional] default is false, if set to true, you can sort on any number of columns at the same time */

    filter: {},                /** [Optional]
                                *  Object { 
                                *              match: string, 
                                *              caseSensitive: true/false, // if not provided, defaults to false
                                *              property: ""               // If provided, will search only in given colum, 
                                *                                            defaults to all columns
                                *         }
                                */

    pagination: {},            /**
                                 * Object { 
                                 *              page: number, (Not zero-based, so starts at 1)
                                 *              itemsPerPage: number
                                 *        }
                                 */
}
```

# Use with a framework like Vue
Kea components are a result of years of development to be flexible and can be used in any modern frontend framework.
In this example I will show you how to add Kea components to a Vue3 / Vite project. This can also be done with other frameworks.
Check the corresponding manual to do that.

**Vue3 example:**
```javascript
/** https://vite.dev/config/ */
export default defineConfig({
  plugins: [
    vue({
      template: {
        compilerOptions: {
          isCustomElement: (tag) => tag.startsWith('kea-')
        }
      }
    }), 
  ]
  ...
});
```

**External resource**

[Add web components in Vue3](https://vuejs.org/guide/extras/web-components.html)
