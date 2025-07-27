---
chapter: Ibiss UI
index: ibiss-ui
icon: "IbissUI.png"
title: Customization
layout: template
toc:
    - Customization
    - Explanation
    - Code example
--- 

# Customization

The core in the designing process of Ibiss UI is to make customizing the colors, the font and distances so simple, that you can just do it in the browser!
This is why I use CSS variables. You can add the CSS in the head and then just add the following on after that to override:


```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo page</title>
    <link rel="stylesheet" href="/assets/css/ibiss-ui.min.css" />

    <style>

        body {
            font-family: Arial;
        }

        :root {
            --primary: green;
        }
    </style>
  </head>

  <body>
    ...
  </body>

</html>
```

In this example it will make your primary color green. The global font is set on the body, if you change that like in the example, it changes for everything, it is that easy!
Here are all the variables you can alter:


## Explanation
{: .mt-3}

| Variable                            |  Description          |
| :---------------------------------- | :---------------------|
|  --html-background: #faf9f8;      | default background color|
|  --background: #fff;                | Background color for inputs and table|
|  --code-background: #f3f2f1;      | Background color for code. |
|                                     |                             |
|  --shadow-color: 0, 0, 0;           | Shadow color for table and shadow utilities |
|  --hr-color: #d2d0ce;             | Color used in the hr element |
|  --border-color: #8a8886;         | Used as default border color |
|                                     | |
|  --primary: #0078d4;              | Color for all primary elements |
|  --primary-hover: #106ebe;        | Hover color for all primary element |
|  --primary-active: #004578;       | Color for active state of the primary element |
|  --color-on-primary: #fff;          | Text color to use on primary background|
|                                     | |
|  --highlight: #fce100;            | Color for the marked html element |
|                                     | |
|  --danger: #d13438;               | Color for all danger elements |
|  --danger-hover: #a92b1a;         | Hover color for all danger element |
|  --danger-active: #740912;        | Color for active state of the danger element |
|  --color-on-danger: #fff;           | Text color to use on danger background|
|                                     | |
|  --warning: #fff4ce;              | Variable for future use in notification |
|  --color-on-warning: #323130;     | |
|                                     | |
|  --error: #fde7e9;                | Variable for future use in notification |
|  --color-on-error: #323130;       | |
|                                     | |
|  --success: #dff6dd;              | Variable for future use in notification |
|  --color-on-success: #323130;     | |
|                                     | |
|  --disabled: #d2d0ce;             | Background color used disabled elements |
|  --color-on-disabled: #a19f9d;    | Text color used on disabled elements |
|                                     | |
|  --button-background: #fff;         | Default button background color |
|  --button-hover: #e1dfdd;         | Default button hover background color |
|  --button-active: #c8c4c4;        | Default button active background color |
|  --button-outline-color: #000;      | Default button focus outline color |
|  --button-color: #000;              | Default text color for buttons |
|                                     | |
|  --disabled-button-background: #f3f2f1;     | Default disabled button background color |
|  --disabled-button-color: #a19f9d;          | Default disabled button text color |
|                                               | |
|  --input-border-color: #605e5c;             | Border color for inputs |
|  --input-hover: #c8c6c4;                    | Input hover color |
|                                               | |
|  --range-track-color: #c8c6c4;              | Base range track color |
|  --range-filled-track-color: #605e5c;       | Filled range color |
|                                               | |
|  --table-hover: #e1dfdd;                    | Table hover color |
|  --table-striped-hover: #d2d0ce;            | Table stripe hover color |
|  --table-stripe: #edebe9;                   | Table stripe color |
|                                               | |
|  --gray: #c8c6c4;                           | Used in color utiliy classes |
|  --color-on-gray: #000;                       | Color used when the background utility is used |
|                                               ||
|  --black: #000;                               | Used in color utiliy classes |
|  --color-on-black: #fff;                      | Color used when the background utility is used |
|                                               | |
|  --white: #fff;                               | Used in color utiliy classes |
|  --color-on-white: #323130;                 | Color used when the background utility is used |
|                                               |
|  --yellow: #fce100;                         | Used in color utiliy classes |     
|  --color-on-yellow: #000;                     | Color used when the background utility is used |     
|                                               |                                              |
|  --orange: #ff9414;                         | Used in color utiliy classes |
|  --color-on-orange: #000;                     | Color used when the background utility is used |
|                                               |
|  --red: #a80000;                            | Used in color utiliy classes |
|  --color-on-red: #fff;                        | Color used when the background utility is used |
|                                               ||
|  --green: #107c10;                          | Used in color utiliy classes |
|  --color-on-green: #fff;                      | Color used when the background utility is used |
|                                               | |
| --distance-1: 0.5rem;                         | Distance used in paddings, margins and gaps |
| --distance-2: 1rem;                           | Distance used in paddings, margins and gaps |
| --distance-3: 1.5rem;                         | Distance used in paddings, margins and gaps |
| --distance-4: 2rem;                           | Distance used in paddings, margins and gaps |
| --distance-5: 2.5rem;                         | Distance used in paddings, margins and gaps |
|                                               | |
| --h1-font-size: 3.2rem;                       | Font size in header and utility class |
| --h2-font-size: 3rem;                         | Font size in header and utility class |
| --h3-font-size: 2.8rem;                       | Font size in header and utility class |
| --h4-font-size: 2.6rem;                       | Font size in header and utility class |
| --h5-font-size: 2.4rem;                       | Font size in header and utility class |
| --h6-font-size: 2.2rem;                       | Font size in header and utility class |
| --th-font-size: 2.2rem;                       | Font size in header and utility class |
| --paragraph-font-size: 1.6rem;                | Font size in header and utility class |
| --label-font-size: 1.6rem;                    | Font size in header and utility class |
| --small-font-size: 1.2rem;                    | Font size in header and utility class |
|                                               | |
| --font-weight-normal: 400;                    | Font weight used for default text and utility |
| --font-weight-semibold: 600;                  | Font weight used for h4, h5, h6 and for the utility class |
| --font-weight-bold: 700;                      | Font weight used for h1, h2, h3, bold, strong and utility class |
|                                               | |
| --line-height-1: 1;                           | Used in the utility class |
| --line-height-2: 1.125;                       | Used in the utility class |
| --line-height-3: 1.25;                        | Used in the utility class |
| --line-height-4: 1.5;                         | Used in the utility class |
{: .table }


## Code example
{: .mt-3}

```css
:root {
  --html-background: #faf9f8;
  --background: #fff;
  --code-background: #f3f2f1;

  --shadow-color: 0, 0, 0;
  --hr-color: #d2d0ce;
  --border-color: #8a8886;

  /** theme colors **/
  --primary: #0078d4;
  --primary-hover: #106ebe;
  --primary-active: #004578;
  --color-on-primary: #fff;

  --highlight: #fce100;

  --danger: #d13438;
  --danger-hover: #a92b1a;
  --danger-active: #740912;
  --color-on-danger: #fff;

  --warning: #fff4ce;
  --color-on-warning: #323130;

  --error: #fde7e9;
  --color-on-error: #323130;

  --success: #dff6dd;
  --color-on-success: #323130;

  --disabled: #d2d0ce;
  --color-on-disabled: #a19f9d;

  /** inputs and buttons **/
  --button-background: #fff;
  --button-hover: #e1dfdd;
  --button-active: #c8c4c4;
  --button-outline-color: #000;
  --button-color: #000;

  --disabled-button-background: #f3f2f1;
  --disabled-button-color: #a19f9d;

  --input-border-color: #605e5c;
  --input-hover: #c8c6c4;

  --range-track-color: #c8c6c4;
  --range-filled-track-color: #605e5c;
  --range-track-hover-color: #e0f2ff;

  /** table **/
  --table-hover: #e1dfdd;
  --table-striped-hover: #d2d0ce;
  --table-stripe: #edebe9;

  /** additional colors **/
  --gray: #c8c6c4;
  --color-on-gray: #000;

  --black: #000;
  --color-on-black: #fff;

  --white: #fff;
  --color-on-white: #323130;

  --yellow: #fce100;
  --color-on-yellow: #000;

  --orange: #ff9414;
  --color-on-orange: #000;

  --red: #a80000;
  --color-on-red: #fff;

  --green: #107c10;
  --color-on-green: #fff;

  /** distances **/
  --distance-1: 0.5rem;
  --distance-2: 1rem;
  --distance-3: 1.5rem;
  --distance-4: 2rem;
  --distance-5: 2.5rem;

  /** typography | 1 rem = 10 px **/
  --h1-font-size: 3.2rem;
  --h2-font-size: 3rem;
  --h3-font-size: 2.8rem;
  --h4-font-size: 2.6rem;
  --h5-font-size: 2.4rem;
  --h6-font-size: 2.2rem;
  --th-font-size: 2.2rem;
  --paragraph-font-size: 1.6rem;
  --label-font-size: 1.6rem;
  --small-font-size: 1.2rem;

  --font-weight-normal: 400;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;

  --line-height-1: 1;
  --line-height-2: 1.125;
  --line-height-3: 1.25;
  --line-height-4: 1.5;
}

```