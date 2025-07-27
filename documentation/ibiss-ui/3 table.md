---
chapter: Ibiss UI
index: ibiss-ui
icon: "IbissUI.png"
title: Table
layout: template
toc:
    - =Examples
    - Default
    - Hover
    - Table
    - Sticky header and table container
    - Table and striped
--- 

# Table classes

These classes are designed to be used either together or separate. A default table has no lines, only spaces.

| Class                        | Effect                                                           | Code 
 :---------------------------- | :--------------------------------------------------------------- | :---------------------------- |
| table                        | Adds a border around the table rows, footer becomes smaller and italic | ```<table class="table">``` |
| hover                        | Adds a color on the row where you hover your mouse               | ```<table class="hover">```       |
| sticky-header                | Can be used with table container. It makes the header be sticky. | ```<table class="sticky-header">```|
| striped                      | Adds zebra stripe to the table in grey/white                     | ```<table class="striped">``` |
| align-top                    | Aligns all the table cells in the body to the top   | ```<table class="align-top">``` |
| align-middle                 | Aligns all the table cells in the body to the middle   | ```<table class="align-middle">``` |
| align-bottom                 | Aligns all the table cells in the body to the bottom   | ```<table class="align-bottom">``` |
|
| **Container class:** 
| table-container              | Just add the specified height and use the sticky-header to get a nice scrollable table | ```<div class="table-container" style="height:12vh;"></div>``` | 
{: .table .align-middle }


# Examples
{: .mb-5 }

## Default
<hr />

<table>
    <thead>
    <tr>
        <th>Column header 1</th>
        <th>Column header 2</th>
        <th>Column header 3</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
    </tr>
    <tr>
        <td>D</td>
        <td>E</td>
        <td>F</td>
    </tr>
    <tr>
        <td>G</td>
        <td>H</td>
        <td>I</td>
    </tr>
    </tbody>
    <tfoot>
    <tr>
        <td colspan="3">Table footer with colspan 3</td>
    </tr>
    </tfoot>
</table>



## Hover
{: .mt-5}
<hr />

<table class="hover">
    <thead>
    <tr>
        <th>Column header 1</th>
        <th>Column header 2</th>
        <th>Column header 3</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
    </tr>
    <tr>
        <td>D</td>
        <td>E</td>
        <td>F</td>
    </tr>
    <tr>
        <td>G</td>
        <td>H</td>
        <td>I</td>
    </tr>
    </tbody>
    <tfoot>
    <tr>
        <td colspan="3">Table footer with colspan 3</td>
    </tr>
    </tfoot>
</table>


## Table
{: .mt-5}
<hr />

<table class="table">
    <thead>
    <tr>
        <th>Column header 1</th>
        <th>Column header 2</th>
        <th>Column header 3</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
    </tr>
    <tr>
        <td>D</td>
        <td>E</td>
        <td>F</td>
    </tr>
    <tr>
        <td>G</td>
        <td>H</td>
        <td>I</td>
    </tr>
    </tbody>
    <tfoot>
    <tr>
        <td colspan="3">Table footer with colspan 3</td>
    </tr>
    </tfoot>
</table>

## Sticky header and table container
{: .mt-5}
<hr />

<div>
<div class="table-container"
        style="height: 12vh">
    <table class="table sticky-header">
    <thead>
        <tr>
        <th>Column 1</th>
        <th>Column 2</th>
        <th>Column 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
        </tr>
        <tr>
        <td>D</td>
        <td>E</td>
        <td>F</td>
        </tr>
        <tr>
        <td>G</td>
        <td>H</td>
        <td>I</td>
        </tr>
        <tr>
        <td>J</td>
        <td>K</td>
        <td>L</td>
        </tr>
        <tr>
        <td>M</td>
        <td>N</td>
        <td>O</td>
        </tr>
        <tr>
        <td>P</td>
        <td>Q</td>
        <td>R</td>
        </tr>
        <tr>
        <td>S</td>
        <td>T</td>
        <td>U</td>
        </tr>
        <tr>
        <td>V</td>
        <td>W</td>
        <td>X</td>
        </tr>
        <tr>
        <td>Y</td>
        <td>Z</td>
        <td>-</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
        <td colspan="3">Table footer with colspan 3</td>
        </tr>
    </tfoot>
    </table>
</div>
</div>


## Table and striped
{: .mt-5}
<hr />

<table class="table striped">
    <thead>
    <tr>
        <th>Column header 1</th>
        <th>Column header 2</th>
        <th>Column header 3</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
    </tr>
    <tr>
        <td>D</td>
        <td>E</td>
        <td>F</td>
    </tr>
    <tr>
        <td>G</td>
        <td>H</td>
        <td>I</td>
    </tr>
    </tbody>
</table>