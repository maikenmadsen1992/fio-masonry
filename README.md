# fio-masonry

## Install
```
npm install fio-masonry
```

## Usage
In the component where you want to use it:
```
import masonry from "fio-masonry";
```
If you want to use the css provided you have to add the following under the import:
```
import 'fio-masonry/dist/fio-masonry.css';
```

### Props/attributes
```
<masonry :items="dateItems" :horizontalCount="count" v-on:clickedItem="itemHaveBeenClciked"/>
```
1. horizontalCount represent the horizontal columns presented. Parse a number (integer)
2. clickedItem is the item the user have pressed in the masonry grid
3. items is an array of objects looking like:

```
{
    'image': 'imgUrl',
    'title': 'Here is 1 title',
    'desc': 'Here is a small description of the image',
    'value': 'here is the oppertunity to parse other informations'
},
{
    'image': 'imgUrl',
    'title': 'Here is 2 title',
    'desc': 'Here is a small description of the image',
    'value': 'here is the oppertunity to parse other informations'
},
{
    'image': 'imgUrl',
    'title': 'Here is 3 title',
    'desc': 'Here is a small description of the image',
    'value': 'here is the oppertunity to parse other informations'
},
```
## Example

In the github project src/App.vue a simple example is presented.

### Youtube

Here is a short link with a simple presentation: https://youtu.be/rnaxOiDwGKI


## Github

Link: https://github.com/maikenmadsen1992/fio-breadcrumb