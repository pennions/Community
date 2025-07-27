---
chapter: Ibiss UI
index: ibiss-ui
icon: "IbissUI.png"
title: Flex layout
layout: template
toc:
    - Responsive prefixes explained
    - =Classes
    - Directions and Flow
    - Gap
    - Justify and Align
    - Align self
    - Flex width
--- 

# Flex layout

These css classes have been carefully designed to help you create great layouts with ease.

## Responsive prefixes explained

|  Screen| Prefix  | 415px | 576px | 768px | 992px | 1200px | 1400px |
|:---  | | :-- | :---: | :---: | :---: | :---: | :---:  | :---:  |
|desktop | d* |    |  |  |  | **X** | **X** |
|tablet  | t* |    |  | **X** | **X** |  |  |
|mobile  | m* |  **X** | **X** |  |  |  |  |
{: .table }

# Classes

## Directions and Flow
{: .mt-3 }

| Class          | Applies          | Responsive classes          | 
| :------------- | :--------------- | :------------------------- |
| row            | display: flex, <br/> flex-wrap: wrap; |  |
| column         | display: flex; <br/>  flex-direction: column;|  |
| no-wrap        | flex-wrap: nowrap; |  |
| wrap-reverse   | flex-wrap: wrap-reverse; |  |
| row-reverse    | flex-direction: row-reverse; | drow-reverse, <br/>  trow-reverse, <br/>  mrow-reverse  |
| column-reverse | flex-direction: column-reverse; | dcolumn-reverse, <br/>  tcolumn-reverse, <br/>  mcolumn-reverse |
{: .table }

## Gap
{: .mt-3 }

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

| Class          | Applies          | Responsive classes          | 
| :------------- | :--------------- | :------------------------- |
| gap-0 | gap: var(--distance-0); | tgap-0, <br/> mgap-0 |
| gap-1 | gap: var(--distance-1); | tgap-1, <br/> mgap-1 |
| gap-2 | gap: var(--distance-2); | tgap-2, <br/> mgap-2 |
| gap-3 | gap: var(--distance-3); | tgap-3, <br/> mgap-3 |
| gap-4 | gap: var(--distance-4); | tgap-4, <br/> mgap-4 |
| gap-5 | gap: var(--distance-5); | tgap-5, <br/> mgap-5 |


## Justify and Align
{: .mt-3 }

Top level alignments. Apply these next to row and column.

| Class          | Applies          | Responsive classes          | 
| :------------- | :--------------- | :------------------------- |
| justify-center | justify-content: center; | - |
| justify-around | justify-content: space-around; | - |
| justify-evenly | justify-content: space-evenly; | - |
| justify-between | justify-content: space-between; | - |
| justify-start | justify-content: flex-start; | - |
| justify-end | justify-content: flex-end; | - |
{: .table }

| Class          | Applies          | Responsive classes          | 
| :------------- | :--------------- | :------------------------- |
| align-center | align-items: center; | - |
| align-start | align-items: flex-start; | - |
| align-end | align-items: flex-end; | - |
| align-stretch | align-items: stretch; | - |
| align-between | align-items: space-between; | - |
| align-around | align-items: space-around; | - |
| align-evenly | align-items: space-evenly; | - |
{: .table }


## Align self
{: .mt-3 }
Child level alignments. Apply these on an item that is nested within a row or column:

| Class          | Applies          | Responsive classes          | 
| :------------- | :--------------- | :------------------------- |
| self-align-stretch | align-self: stretch; | - |
| self-align-center | align-self: center; | - |
| self-align-start | align-self: flex-start; | - |
| self-align-end | align-self: flex-end; | - |
{: .table }


## Flex width
{: .mt-3 }

These utility classes help you divide the child items with ease. If you have a column direction it will be used as height, else it will be used as width

| Class          | Applies          | Responsive classes          | 
| :------------- | :--------------- | :------------------------- |
| f-100 | flex: 0 0 100%;           | tf-100, <br/> mf-100 |
| f-50 | flex: 0 0 calc(100% / 2);  | tf-50, <br/> mf-50  |
| f-33 | flex: 0 0 calc(100% / 3);  | tf-33 <br/> mf-33  |
| f-25 | flex: 0 0 calc(100% / 4);  | tf-25, <br/> mf-25  |
| f-20 | flex: 0 0 calc(100% / 5);  | tf-20, <br/> mf-20  |
| f-16 | flex: 0 0 calc(100% / 8);  | tf-16, <br/> mf-16  |
| f-10 | flex: 0 0 calc(100% / 10); | tf-10, <br/> mf-10  |
| f-8 | flex: 0 0 calc(100% / 12);  | tf-8, <br/> mf-8  |
| f-auto | flex: 1 1 auto; <br /> min-width: auto; <br /> width: initial; <br />  max-width: fit-content; | tf-auto, <br/> mf-auto |
| f-fill | flex: 1; <br /> min-width: initial; <br /> width: 100%; <br /> max-width: initial; | tf-fill, <br/> mf-fill |
{: .table }
