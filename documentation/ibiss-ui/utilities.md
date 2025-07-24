---
chapter: Ibiss UI
index: ibiss-ui
icon: "IbissUI.png"
title: Utilities
layout: template
filename: utilities
toc: 
    - Paddings
    - Margins
    - Shadows
    - Borders
    - Cursors
    - =Display
    - Responsive Hide and Show
    - =Colors
    - Text and Icons
    - Borders
    - Backgrounds
--- 

# Utilities

Here are all the utility classes that help customize your website or application

**Responsive prefixes explained**

| Screen | Prefix  | 415px | 576px | 768px | 992px | 
|:---    | :--     | :---: | :---: | :---: | :---: | 
|tablet  | t*      |       |       | **X** | **X** | 
|mobile  | m*      |  **X** | **X** |      |       |  
{: .table }

<small><i>Example .mpd-0 for mobile padding 0 or .tm-0 for tablet margin 0 </i></small>



# Paddings
{:mt-3}

These are the default sizes, you can adjust them with CSS variables:

```css
:root {
    --distance-0: 0;
    --distance-1: 0.5rem;
    --distance-2: 1rem;
    --distance-3: 1.5rem;
    --distance-4: 2rem;
    --distance-5: 2.5rem;
}
```

| Padding class          | Applies          | Responsive classes | 
| :------------- | :--------------- | :------------------------- |
| m-0            | padding: var(--distance-0); | tm-0 <br/> mm-0  |
| m-1            | padding: var(--distance-1); | tm-1 <br/> mm-1  |
| m-2            | padding: var(--distance-2); | tm-2 <br/> mm-2  |
| m-3            | padding: var(--distance-3); | tm-3 <br/> mm-3  |
| m-4            | padding: var(--distance-4); | tm-4 <br/> mm-4  |
| m-5            | padding: var(--distance-5); | tm-5 <br/> mm-5  |
||||
| **Padding left** |                           |                |
| pl-0            | padding-left: var(--distance-0); | tpl-0 <br/> mpl-0  |
| pl-1            | padding-left: var(--distance-1); | tpl-1 <br/> mpl-1  |
| pl-2            | padding-left: var(--distance-2); | tpl-2 <br/> mpl-2  |
| pl-3            | padding-left: var(--distance-3); | tpl-3 <br/> mpl-3  |
| pl-4            | padding-left: var(--distance-4); | tpl-4 <br/> mpl-4  |
| pl-5            | padding-left: var(--distance-5); | tpl-5 <br/> mpl-5  |
| pl-auto         | padding-left: auto;              | tpl-auto <br/> mpl-auto  |
||||
| **Padding right** |                           |                |
| pr-0            | padding-right: var(--distance-0); | tpr-0 <br/> mpr-0  |
| pr-1            | padding-right: var(--distance-1); | tpr-1 <br/> mpr-1  |
| pr-2            | padding-right: var(--distance-2); | tpr-2 <br/> mpr-2  |
| pr-3            | padding-right: var(--distance-3); | tpr-3 <br/> mpr-3  |
| pr-4            | padding-right: var(--distance-4); | tpr-4 <br/> mpr-4  |
| pr-5            | padding-right: var(--distance-5); | tpr-5 <br/> mpr-5  |
| pr-auto         | padding-right: auto;              | tpr-auto <br/> mpr-auto  |
||||
| **Padding top** |                           |                |
| pt-0            | padding-top: var(--distance-0); | tpt-0 <br/> mpt-0  |
| pt-1            | padding-top: var(--distance-1); | tpt-1 <br/> mpt-1  |
| pt-2            | padding-top: var(--distance-2); | tpt-2 <br/> mpt-2  |
| pt-3            | padding-top: var(--distance-3); | tpt-3 <br/> mpt-3  |
| pt-4            | padding-top: var(--distance-4); | tpt-4 <br/> mpt-4  |
| pt-5            | padding-top: var(--distance-5); | tpt-5 <br/> mpt-5  |
| pt-auto         | padding-top: auto;              | tpt-auto <br/> mpt-auto  |
||||
| **Padding bottom** |                           |                |
| pb-0            | padding-bottom: var(--distance-0); | tpb-0 <br/> mpb-0  |
| pb-1            | padding-bottom: var(--distance-1); | tpb-1 <br/> mpb-1  |
| pb-2            | padding-bottom: var(--distance-2); | tpb-2 <br/> mpb-2  |
| pb-3            | padding-bottom: var(--distance-3); | tpb-3 <br/> mpb-3  |
| pb-4            | padding-bottom: var(--distance-4); | tpb-4 <br/> mpb-4  |
| pb-5            | padding-bottom: var(--distance-5); | tpb-5 <br/> mpb-5  |
| pb-auto         | padding-bottom: auto;              | tpb-auto <br/> mpb-auto  |
||||
| **Padding left and right** |                           |                |
| px-0            | padding-left: var(--distance-0); <br/> padding-right: var(--distance-0);  | tpx-0 <br/> mpx-0  |
| px-1            | padding-left: var(--distance-1); <br/> padding-right: var(--distance-1);  | tpx-1 <br/> mpx-1  |
| px-2            | padding-left: var(--distance-2); <br/> padding-right: var(--distance-2);  | tpx-2 <br/> mpx-2  |
| px-3            | padding-left: var(--distance-3); <br/> padding-right: var(--distance-3);  | tpx-3 <br/> mpx-3  |
| px-4            | padding-left: var(--distance-4); <br/> padding-right: var(--distance-4);  | tpx-4 <br/> mpx-4  |
| px-5            | padding-left: var(--distance-5); <br/> padding-right: var(--distance-5);  | tpx-5 <br/> mpx-5  |
| px-auto         | padding-left: auto; <br/> padding-right: auto;  | tpx-auto <br/> mpx-auto  |
||||
| **Padding top and bottom** |                           |                |
| py-0            | padding-top: var(--distance-0); <br/> padding-bottom: var(--distance-0);  | tpy-0 <br/> mpy-0  |
| py-1            | padding-top: var(--distance-1); <br/> padding-bottom: var(--distance-1);  | tpy-1 <br/> mpy-1  |
| py-2            | padding-top: var(--distance-2); <br/> padding-bottom: var(--distance-2);  | tpy-2 <br/> mpy-2  |
| py-3            | padding-top: var(--distance-3); <br/> padding-bottom: var(--distance-3);  | tpy-3 <br/> mpy-3  |
| py-4            | padding-top: var(--distance-4); <br/> padding-bottom: var(--distance-4);  | tpy-4 <br/> mpy-4  |
| py-5            | padding-top: var(--distance-5); <br/> padding-bottom: var(--distance-5);  | tpy-5 <br/> mpy-5  |
| py-auto         | padding-top: auto; <br/> padding-bottom: auto;  | tpy-auto <br/> mpy-auto  |
{: .table }


# Margins
{:mt-3}

These are the default sizes, you can adjust them with CSS variables:

```css
:root {
    --distance-0: 0;
    --distance-1: 0.5rem;
    --distance-2: 1rem;
    --distance-3: 1.5rem;
    --distance-4: 2rem;
    --distance-5: 2.5rem;
}
```

| Margin class          | Applies          | Responsive classes | 
| :------------- | :--------------- | :------------------------- |
| m-0            | margin: var(--distance-0); | tm-0 <br/> mm-0  |
| m-1            | margin: var(--distance-1); | tm-1 <br/> mm-1  |
| m-2            | margin: var(--distance-2); | tm-2 <br/> mm-2  |
| m-3            | margin: var(--distance-3); | tm-3 <br/> mm-3  |
| m-4            | margin: var(--distance-4); | tm-4 <br/> mm-4  |
| m-5            | margin: var(--distance-5); | tm-5 <br/> mm-5  |
||||
| **Margin left** |                           |                |
| ml-0            | margin-left: var(--distance-0); | tml-0 <br/> mml-0  |
| ml-1            | margin-left: var(--distance-1); | tml-1 <br/> mml-1  |
| ml-2            | margin-left: var(--distance-2); | tml-2 <br/> mml-2  |
| ml-3            | margin-left: var(--distance-3); | tml-3 <br/> mml-3  |
| ml-4            | margin-left: var(--distance-4); | tml-4 <br/> mml-4  |
| ml-5            | margin-left: var(--distance-5); | tml-5 <br/> mml-5  |
| ml-auto         | margin-left: auto;              | tml-auto <br/> mml-auto  |
||||
| **Margin right** |                           |                |
| mr-0            | margin-right: var(--distance-0); | tmr-0 <br/> mmr-0  |
| mr-1            | margin-right: var(--distance-1); | tmr-1 <br/> mmr-1  |
| mr-2            | margin-right: var(--distance-2); | tmr-2 <br/> mmr-2  |
| mr-3            | margin-right: var(--distance-3); | tmr-3 <br/> mmr-3  |
| mr-4            | margin-right: var(--distance-4); | tmr-4 <br/> mmr-4  |
| mr-5            | margin-right: var(--distance-5); | tmr-5 <br/> mmr-5  |
| mr-auto         | margin-right: auto;              | tmr-auto <br/> mmr-auto  |
||||
| **Margin top** |                           |                |
| mt-0            | margin-top: var(--distance-0); | tmt-0 <br/> mmt-0  |
| mt-1            | margin-top: var(--distance-1); | tmt-1 <br/> mmt-1  |
| mt-2            | margin-top: var(--distance-2); | tmt-2 <br/> mmt-2  |
| mt-3            | margin-top: var(--distance-3); | tmt-3 <br/> mmt-3  |
| mt-4            | margin-top: var(--distance-4); | tmt-4 <br/> mmt-4  |
| mt-5            | margin-top: var(--distance-5); | tmt-5 <br/> mmt-5  |
| mt-auto         | margin-top: auto;              | tmt-auto <br/> mmt-auto  |
||||
| **Margin bottom** |                           |                |
| mb-0            | margin-bottom: var(--distance-0); | tmb-0 <br/> mmb-0  |
| mb-1            | margin-bottom: var(--distance-1); | tmb-1 <br/> mmb-1  |
| mb-2            | margin-bottom: var(--distance-2); | tmb-2 <br/> mmb-2  |
| mb-3            | margin-bottom: var(--distance-3); | tmb-3 <br/> mmb-3  |
| mb-4            | margin-bottom: var(--distance-4); | tmb-4 <br/> mmb-4  |
| mb-5            | margin-bottom: var(--distance-5); | tmb-5 <br/> mmb-5  |
| mb-auto         | margin-bottom: auto;             | tmb-auto <br/> mmb-auto  |
||||
| **Margin left and right** |                           |                |
| mx-0            | margin-left: var(--distance-0); <br/> margin-right: var(--distance-0);  | tmx-0 <br/> mmx-0  |
| mx-1            | margin-left: var(--distance-1); <br/> margin-right: var(--distance-1);  | tmx-1 <br/> mmx-1  |
| mx-2            | margin-left: var(--distance-2); <br/> margin-right: var(--distance-2);  | tmx-2 <br/> mmx-2  |
| mx-3            | margin-left: var(--distance-3); <br/> margin-right: var(--distance-3);  | tmx-3 <br/> mmx-3  |
| mx-4            | margin-left: var(--distance-4); <br/> margin-right: var(--distance-4);  | tmx-4 <br/> mmx-4  |
| mx-5            | margin-left: var(--distance-5); <br/> margin-right: var(--distance-5);  | tmx-5 <br/> mmx-5  |
| mx-auto         | margin-left: auto; <br/> margin-right: auto;  | tmx-auto <br/> mmx-auto  |
||||
| **Margin top and bottom** |                           |                |
| my-0            | margin-top: var(--distance-0); <br/> margin-bottom: var(--distance-0);  | tmy-0 <br/> mmy-0  |
| my-1            | margin-top: var(--distance-1); <br/> margin-bottom: var(--distance-1);  | tmy-1 <br/> mmy-1  |
| my-2            | margin-top: var(--distance-2); <br/> margin-bottom: var(--distance-2);  | tmy-2 <br/> mmy-2  |
| my-3            | margin-top: var(--distance-3); <br/> margin-bottom: var(--distance-3);  | tmy-3 <br/> mmy-3  |
| my-4            | margin-top: var(--distance-4); <br/> margin-bottom: var(--distance-4);  | tmy-4 <br/> mmy-4  |
| my-5            | margin-top: var(--distance-5); <br/> margin-bottom: var(--distance-5);  | tmy-5 <br/> mmy-5  |
| my-auto         | margin-top: auto; <br/> margin-bottom: auto;  | tmy-auto <br/> mmy-auto  |
{: .table }

# Shadows

| Example                                                  | Class | Code                                                        | 
| :-------------                                           |:--- |:-------------------------                                 |
| <div class="shadow py-5 px-3 my-3 mr-3">Element with shadow</div>| shadow   |```<div class="shadow py-5 px-3">Element with shadow</div>``` |
| <div class="shadow-top py-5 px-3 my-3 mr-3">Element with shadow on top</div>| shadow-top   |```<div class="shadow py-5 px-3">Element with shadow on top</div>``` |
| <div class="shadow-left py-5 px-3 my-3 mr-3">Element with shadow on left</div> | shadow-left   |```<div class="shadow py-5 px-3">Element with shadow on the left</div>``` |
| <div class="shadow-right py-5 px-3 my-3 mr-3">Element with shadow on right</div>|shadow-right   |```<div class="shadow py-5 px-3">Element with shadow on the right</div>``` |
| <div class="shadow-bottom py-5 px-3 my-3 mr-3">Element with shadow on bottom</div>|shadow-bottom   |```<div class="shadow py-5 px-3">Element with shadow on the bottom</div>``` |
|||
|  **Large variants**       | |
| <div class="shadow-lg py-5 px-3 my-3 mr-3">Element with large shadow</div>| shadow-lg   |```<div class="shadow-lg py-5 px-3">Element with large shadow</div>``` |
| <div class="shadow-lg-top py-5 px-3 my-3 mr-3">Element with large shadow on top</div>| shadow-lg-top   |```<div class="shadow-lg-top py-5 px-3">Element with large shadow on top</div>``` |
| <div class="shadow-lg-left py-5 px-3 my-3 mr-3">Element with large shadow on left</div>| shadow-lg-left   |```<div class="shadow-lg-left py-5 px-3">Element with large shadow on the left</div>``` |
| <div class="shadow-lg-right py-5 px-3 my-3 mr-3">Element with large shadow on right</div>| shadow-lg-right   |```<div class="shadow-lg-right py-5 px-3">Element with large shadow on the right</div>``` |
| <div class="shadow-lg-bottom py-5 px-3 my-3 mr-3">Element with large shadow on bottom</div>| shadow-lg-bottom   |```<div class="shadow-lg-bottom py-5 px-3">Element with large shadow on the bottom</div>``` |
{: .table .example-table }

# Borders 

| Example                                                                           | Class        | Code |
| :------------- | :-------------------------                                       |:--| :-----------------------         |
| <div class="border py-5 px-3 my-3 mr-3">Element with border</div>                      | border   |```<div class="border py-5 px-3">Element with border</div>``` |
| <div class="border-top py-5 px-3 my-3 mr-3">Element with border on top</div>           | border-top   |```<div class="border-top py-5 px-3">Element with border on top</div>``` |
| <div class="border-left py-5 px-3 my-3 mr-3">Element with border on the left</div>     | border-left   |```<div class="border-left py-5 px-3">Element with border on the left</div>``` |
| <div class="border-right py-5 px-3 my-3 mr-3">Element with border on the right</div>   | border-right   |```<div class="border-right py-5 px-3">Element with border on the right</div>``` |
| <div class="border-bottom py-5 px-3 my-3 mr-3">Element with border on the bottom</div> | border-bottom   |```<div class="border-bottom py-5 px-3">Element with border on the bottom</div>``` |
{: .table .example-table }

# Cursors

| Example        |Class|  Code                                                        | 
| :------------- |:---------------------- | :-------------------------                                 |
| <div class="border p-1 pl-3 cursor-not-allowed">Hover me, cursor turns to not allowed</div>  | cursor-not-allowed | ```<div class="border p-1 pl-3 cursor-not-allowed">Hover me, cursor turns to not allowed</div>``` |
| <div class="border p-1 pl-3 cursor-pointer">Hover me, cursor turns to pointer</div>| cursor-pointer | ```<div class="border p-1 pl-3 cursor-pointer">Hover me, cursor turns to pointer</div>```|
| <div class="border p-1 pl-3 cursor-grab">Hover me, cursor turns to grab</div>| cursor-grab | ```<div class="border p-1 pl-3 cursor-grab">Hover me, cursor turns to grab</div>```|
| <div class="border p-1 pl-3 cursor-grabbing">Hover me, cursor turns to grabbing</div>| cursor-grabbing | ```<div class="border p-1 pl-3 cursor-grabbing">Hover me, cursor turns to grabbing</div>```|
| <div class="border p-1 pl-3 cursor-zoom-in"> Hover me, cursor magnifying glass [+]</div>| cursor-zoom-in | ```<div class="border p-1 pl-3 cursor-zoom-in"> Hover me, cursor turns to magnifying glass [+]</div>```|
| <div class="border p-1 pl-3 cursor-zoom-out"> Hover me, cursor magnifying glass [-] </div>| cursor-zoom-out | ```<div class="border p-1 pl-3 cursor-zoom-out"> Hover me, cursor turns to magnifying glass [-] </div>```|
| <div class="border p-1 pl-3 cursor-wait">Hover me, cursor waiting </div>| cursor-wait | ```<div class="border p-1 pl-3 cursor-wait">Hover me, cursor turns to spinner or hourglass depending on the browser </div>```|
| <div class="border p-1 pl-3 cursor-help">Hover me, cursor help icon</div>| cursor-help | ```<div class="border p-1 pl-3 cursor-help">Hover me, cursor turns to help icon</div>```|
| <div class="border p-1 pl-3 cursor-default">Makes the cursor to be the default arrow.</div>| cursor-default | ```<div class="border p-1 pl-3 cursor-default">Makes the cursor to be the default arrow.</div>```|
| <div class="border p-1 pl-3 cursor-no-select">Makes the cursor unable to select text.</div>| cursor-no-select | ```<div class="border p-1 pl-3 cursor-no-select">Makes the cursor unable to select text.</div>```|
{: .table .example-table }

# Display

## Responsive Hide and Show

|  Class     | 415px | 576px | 768px | 992px | 1200px | 1400px |
|:---          | :--   | :---: | :---: | :---: | :---: | :---:   | 
|desktop       |       |       |       |       | **X** | **X**   |
|tablet        |       |       | **X** | **X** |       |         |
|mobile        | **X** | **X** |       |       |       |         |
|small-screen  | **X** | **X** |  **X**|       |       |         |
|large-screen  |       |       |       |**X**  |**X**  |**X**    |
{: .table }

 <div class="column mt-3">
    <span class="mb-3">Resize the screen to see it in action:</span>
    <div class="mobile bg-danger p-3">Mobile</div>
    <div class="tablet bg-accent p-3">Tablet</div>
    <div class="desktop bg-primary p-3">desktop</div>
    <div class="small-screen bg-gray p-3">small-screen</div>
    <div class="large-screen bg-gray-dark p-3">large-screen</div>
</div>
      

# Colors

## Text and Icons

## Borders

## Backgrounds
