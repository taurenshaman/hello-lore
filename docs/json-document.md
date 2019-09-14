# JSON document
You can write note in JSON format.

## Templates
We have defined several [JSON templates](https://github.com/13f/templates):  
* Bookmark
* Money: payment/income
* Collection
* todo/task

## Visualization
1. By default, there must be a **JSON code view** with highlight supported.  
```$("#jsoncode").JSONView(json);```  
1.1 By default, there may be a **[hierarchy view](https://github.com/13f/lore-graph)** for json content, **IF** there is no graph `processor` like `vis/network` or `d3` or `cytoscape`.  

2. If the root has a `items` property and the type its value is array, and the root has a `template` property, there will be a **Template view**.
  The templates currently supported: bookmark

3. If the root has a `items` property and the type its value is array, there will be a **DataTable view**.  
```
// check
bool hasItemsAndIsArray = Model != null && Model.Content.Token["items"] != null && Model.Content.Token["items"].Type == Newtonsoft.Json.Linq.JTokenType.Array;

// json to html table
  if (json["items"] != null) {
      var jsonHtmlTable = ConvertJsonToTable(json["items"], 'jsonTable', 'dataTable', 'Link');
      $("#datatable").append(jsonHtmlTable);
      $("#jsonTable").DataTable();
  }
```

4. If the root has a `processor` property and its value is `vis/network`, there will be a **Vis/Network view**.
5. If the root has a `type` property and its value is `AdaptiveCard`, there will be a **Adaptive Card view**.

## Personal Data
1. Personanl navigation page: /{username}/[navigation|123]  
Based on this project: https://github.com/xcatliu/123


## Tech Stack
Web Frontend:  
[JSON Editor](https://github.com/josdejong/jsoneditor)

Backend database:  
Azure Cosmos DB  
Each document item in the DB has a size limit: [2MB](https://docs.microsoft.com/zh-cn/azure/cosmos-db/concepts-limits#per-item-limits). So each json document has a capacity limit.
