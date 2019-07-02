## Templates
We have defined several [JSON templates](https://github.com/13f/templates):  
* Bookmark
* Money: payment/income
* Collection
* todo/task

## Visualization
1. By default, here is a **JSON code view** with highlight supported.  
```$("#jsoncode").JSONView(json);```  

2. If the root has a `items` property ~~and the type its value is array~~, there will be a **DataTable view**.  
```// json to html table
  if (json["items"] != null) {
      var jsonHtmlTable = ConvertJsonToTable(json["items"], 'jsonTable', 'dataTable', 'Link');
      $("#datatable").append(jsonHtmlTable);
      $("#jsonTable").DataTable();
  }
```

## Personal Data
1. Personanl navigation page: /{username}/[navigation|123]  
Based on this project: https://github.com/xcatliu/123


## Tech Stack
Web Frontend:  
[JSON Editor](https://github.com/josdejong/jsoneditor)

Backend database:  
Azure Cosmos DB  
Each document item in the DB has a size limit: [2MB](https://docs.microsoft.com/zh-cn/azure/cosmos-db/concepts-limits#per-item-limits). So each json document has a capacity limit.
