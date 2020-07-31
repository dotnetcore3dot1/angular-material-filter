
## Angular Mat Table Filtering Sorting Pagination and Button Column


## 1.Install Angular Material
 
 ```
 https://material.angular.io/guide/getting-started
```

## 2.Copy DataTable folder to your source.


## 3.Add DataTable Component to your Module.


## 4.Copy columndef.model.ts file to your source.


## 5.Add following code to your component.ts file

Column Defination  
```
 columns: Array<ColumnDef> = [
    { name: "edit", displayName: `Edit`, columnType: ColumnType.Button, class: `btn btn-primary btn-sm`, defaultText: "<i class='fa fa-pencil'></i>", sort: false },
    { name: "delete", displayName: `Delete`, columnType: ColumnType.Button, class: `btn btn-danger btn-sm`, defaultText: "<i class='fa fa-trash'></i>", sort: false },
    { name: "id", displayName: `Popup`, columnType: ColumnType.Button, class: `btn btn-warning btn-sm` },
    { name: "title", displayName: "Title", width: '200' },
    { name: "body", displayName: "Text", width: '900', class: `text-primary` }
  ];
  ```
  Click Event Handler 
  ```
  HandleClick(values: any) {
    //Compare column name to find clicked column
    if (values.name == 'edit') {     
      let row = values.value;
      console.log(row);
    }
    if (values.name == 'delete') {
      let row = values.value;
      console.log(row);
    }
    if (values.name == 'id') {
      let row = values.value;
      console.log(row);
    }
  }
  ```
  
  
  ## 6.Add following code to your component.html
  
  Replace  dataobject with your data array
  ```
   <datatable [data]="dataobject" [columns]="columns" (rowclick)="HandleClick($event)"></datatable>
  ```
