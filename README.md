A reusable responsive react.js table component with sorting and filtering options. Sorting and filtering can be configurable easily with column items of data. 

## NPM Package
https://www.npmjs.com/package/react-reusable-table

# Demo
https://reusable-table-component.firebaseapp.com/

## Usage

Use react-reusable-table as below.
##
import React from 'react'

import { Table } from 'react-reusable-table'
##

##
const App = () => (
    <div className="App">
<Table
caption=""
data={this.props.records}
detailPage={this.detailPageHandler}
footerCells={utility.getHeaderCells()}
headerCells={utility.getHeaderCells()}
showFooter={false}
sortedUporDown={this.sortRecordsHandler}/>
);
##
  
// utility.js

// getHeaderCells method

##
export const getHeaderCells  =  () =>  {
return [
{ label: 'ID', name: 'id', isFilterAble: false, isSortAble: false },
{ label: 'Status', name: 'status', isFilterAble: true, isSortAble: false },
{ label: 'Machine Type', name: 'machine_type', isFilterAble: true, isSortAble: false },
{ label: 'Longitude', name: 'longitude', isFilterAble: false, isSortAble: true },
{ label: 'Latitude', name: 'latitude', isFilterAble: false, isSortAble: true },
{ label: 'Last Maintenance', name: 'last_maintenance', isFilterAble: false, isSortAble: true },
{ label: 'Install Date', name: 'install_date', isFilterAble: false, isSortAble: true },
{ label: 'Floor', name: 'floor', isFilterAble: true, isSortAble: false }
]
}
##

// sort records in asc or desc order
##
sortRecordsHandler = (colName, sortType) => {
this.props.onSortRecords(colName, sortType);
}
##

//  go to detail page
##
detailPageHandler = (id) => {
        this.props.history.push('records/' + id);
 }
##

// sample records
##
{
	"data": [
{
			"status": "running",
			"machine_type": "microscope",
			"longitude": 48.09540056785246,
			"latitude": 11.523880271993598,
			"last_maintenance": "2017-04-01T15:00:00.000000Z",
			"install_date": "2015-04-18",
			"id": "68015cc1-3119-42d2-9d4e-3e824723fe03",
			"floor": 5
		},
		{
			"status": "running",
			"machine_type": "microscope",
			"longitude": 48.09535029616455,
			"latitude": 11.523869432452495,
			"last_maintenance": "2017-04-01T14:00:00.000000Z",
			"install_date": "2015-04-11",
			"id": "59d9f4b4-018f-43d8-92d0-c51de7d987e5",
			"floor": 4
		}
	]
}
##

## Sorting & Filtering

Sorting and filtering can be configurable using any column items from the records. In the above configurable method getHeaderCells  there are two flags isFilterAble and isSortAble can be set for each of the column items for records. So setting true any of them will enable the filter or sort option for column items.

## Installation
## npm
npm i react-reusable-table --save
## yarn
yarn add react-reusable-table 
 
 
 


