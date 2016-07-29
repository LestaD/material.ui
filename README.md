# material.ui
Another Material UI package

## Readme

> Package now in development
> Please, star it and come back later

## Specification

### Table

https://material.google.com/components/data-tables.html

```javascript
<Table.Paper data={dessertList.toMap()} perPage={10}>
  <Table.Header title="Nutrition" />
  <Table.Header whenFree>
    <Button flat accent>Add</Button>
    <Button flat accent>Remove</Button>
    <Separator />
    <Button flat icon="sort" />
    <Button flat icon="menu_vert" />
  </Table.Header>
  <Table.Header whenSelected>
    <Button flat icon="bucket" />
    <Button flat icon="menu_vert" />
  </Table.Header>
  
  <Table.Check {/* prop="selected" */} onCheck={::this.handleCheckDessert} />
  <Table.Column prop="name" label="Dessert (100g serving)" />
  <Table.Column prop="calories" label="Calories" sort={Table.sort.Number} tooltip="The total amount of food energy" />
  <Table.Column prop="fat" label="Fat (g)" sort={Table.sort.Number} format="00.0" />
  <Table.Column prop="carbs" label="Carbs (g)" sort={Table.sort.Number} />
  <Table.Column prop="comment" label="Comments" icon="message" editable>
    <Input proxy max={140} min={10} validate={value => value.match(/\w+/)} />
  </Table.Column>
</Table.Paper>
```


## Installation

```bash
npm install --save material.ui
```

## Usage

```js
// With webpack and babel

import 'material.ui/styles.css';
import { NavigationBottom, Button, FloatingButton, Chips, Switch } from 'material.ui';
```

```js
// Webpack only

require('material.ui/styles.css');
const { NavigationBottom, Button, FloatingButton, Chips, Switch } = require('material.ui');
```

```js
// Without webpack and babel in the browser
//
// Copy styles.css to your directory
// <link rel="stylesheet" href="/node_modules/material.ui/styles.css" />
// <script src="/node_modules/material.ui/dist/material.ui.js"></script>

var NavigationBottom = MaterialUI;
var Button = MaterialUI;
var FloatingButton = MaterialUI;
var Chips = MaterialUI;
var Switch = MaterialUI;
```
