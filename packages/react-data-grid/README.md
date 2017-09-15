# react-data-grid

> This is a folk version of [react-data-grid](https://github.com/adazzle/react-data-grid) with some enhancements.

## Install

```sh
npm install --save react-data-grid-lei
```

## Enhancements:
	1. Make the editable cell into editing status when focus in.
	```
	quickEdit = true
	``` 
	2. Skip the none-editable cells when press tab or arraw keys:
	```
	focusEditOnly = true
	```

## Usage

 ```sh
import ReactDataGrid from 'react-data-grid-lei';

const columns = [{ key: 'id', name: 'ID' }, { key: 'title', name: 'Title' }];
const rows = [{ id: 1, title: 'Title 1' }, ...];
const rowGetter = rowNumber => rows[rowNumber];

const Grid = () => {
  return <ReactDataGrid
  	quickEdit={true}
  	focusEditOnly={true}
    columns={columns}
    rowGetter={rowGetter}
    rowsCount={rows.length}
    minHeight={500} />);
}
```