# Changelog

## 0.0.14 (26.02.2025)

### Table Filters
- Exposed filterState variable
- Handle onFilterChanged event

## 0.0.13 (25.02.2025)

### Table Filters
- Implemented core filtering functionality and dynamic config.
- Supported filter data type auto detection.

## 0.0.12 (24.02.2025)

### Table Action Buttons
- Implemented switching between Icon and Button in Action Buttons column. Now regular text buttons are also supported with initial styling based on Figma.
- Implemented injecting wwElements as table cells. Image and Text are supported for now.

## 0.0.11 (17.02.2025)

### Table Action Buttons
- Implemented fixed height of table (option + field to provide size)
- Implemented auto height of table (based on calculation of displayed rows height)

## 0.0.10 (17.02.2025)

### Table Action Buttons
- Support of many action buttons instead only three fixed ones.
- Implemented dynamic add/remove/sort action buttons. Icon elements are re-adjusted on add or remove action button.

## 0.0.9 (13.02.2025)

### Table Action Buttons
- Introduced Action Buttons column - pinned to the right side of table.
- Implemented Action Buttons configuration - possibility to dynamically add/remove/sort action buttons
- Implemented possibility of changing an Icon of Action Button (edit, remove, custom - fixed set of icons for now, would be extended by dynamic approach based on configured buttons)
- Implemented triggering a workflow on Action Button click

## 0.0.8 (11.02.2025)

### Table Custom Data Formatter
- Added cell value formatter based on custom script code.

## 0.0.7 (09.02.2025)

### Custom Columns Definition
- Added possibility to set path of column object (auto suggested reference to row object fields)
- Added possibility of defining paths to object nested properties e.g. `row.propertyA.propertyB`
- Added possibility to set manually column cell data type, or stay with automatic detection
- Added possibility to set if column is `sortable` and `visible`
- Added `timestamp` data type formatter

## 0.0.6 (06.02.2025)

### Added component variables
- Exposed `selectedRows` component's variable which keeps an array of currently selected rows (array of data objects).
- Exposed `paginationState` component's variable which keeps an object which represents current state of pagination. It keeps paging metadata.
- Exposed `sortState` component's variable which keeps an array which represents current state of sorting. Columns have theirs sort state.

### Added component events
- Supported `onRowClicked` event. It shares data about clicked row's data and index.
- Supported `onRowDoubleClicked` event. It shares data about clicked row's data and index.
- Supported `onCellClicked` event. It shares data about clicked cell's data and field name. Additionally, it shares corresponding row data.
- Supported `onCellDoubleClicked` event. It shares data about clicked cell's data and field name. Additionally, it shares corresponding row data.
- Supported `onColumnHeaderClicked` event. It shares data about clicked header's name (field name).
