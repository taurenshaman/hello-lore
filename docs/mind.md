# Mind (Map) | 思维导图

There must be one RootNode/MainNode (mainNode: "main") and one ContextNode (contextNode: "context"), and 0 ~ N nodes are normal ones (normalNode: "normal").  

## Context
There is no context at root, but a context node in nodes:
```json
{
    "group": "nodes",
    "data": {
        "id": "",
        "title": "Graph Context",
        "titleColor": "#000000",
        "contextNode": "context",
        "shapeBackgroundColor": "#cc99cc",
        "shapeBorderColor": "#cc99cc",
        "uri": "",
        "description": "",
        "descriptionType": "markdown"
    },
    //...
},
```

## Style
If you wanna use a customized style (TODO), please read the [Default style](https://lore.chuci.info/apps/cytoscape/cytoscape-styles-default.js) for reference. And the following is the structure of node/edge.  

## `data` of element (node/edge)
```json
// node
// There are 3 types of nodes, used for **styles**:
// 1. mainNode: "main"
// 2. contextNode: "context"
// 3. normalNode: "normal"
"data": {
    "id": "{length:32}",
    "title": "{node title}",
    "titleColor": "#000000",
    "normalNode": "normal",
    "shapeBackgroundColor": "#aaccff",
    "shapeBorderColor": "#6699cc",
    "description": "", 
    "descriptionType": "markdown",
    "semantics": [
        {
            "key": "equivalentTo",
            "keyTitle": "Equivalent To",
            "title": "创意思维 #吴迪",
            "uri": "https://lore.chuci.info/manage/edit/mind/c484c82b11c34c7aa9fcf6a2f7c1594d"
        }
    ]
},

// edge
"data": {
    "source": "{id of the source node}",
    "target": "{id of the target node}",
    "id": "{length:32}",
    "title": "{}edge title}",
    "titleColor": "#000000",
    "edgeColor": "#666666",
    "description": "",
    "descriptionType": "markdown",
    "semantics": []
},
```

## semantics
{key, keyTitle, **title**, **uri**}  
You can only set `title` and `uri`.  

### Available semantics
```
reference: { key: "reference", keyTitle: "Reference" }, // 参考，引用
isA: { key: "isA", keyTitle: "Is A" }, // 指明Type/类型
equivalentTo: { key: "equivalentTo", keyTitle: "Equivalent To" }, // 等价于
extendedFrom: { key: "extendedFrom", keyTitle: "Extended From" }, // 引申自
derivedFrom: { key: "derivedFrom", keyTitle: "Derived From" }, // 继承自
```

## Tech Stack
Web Frontend: 
[cytoscape.js](https://js.cytoscape.org/)  
[tui.editor](https://github.com/nhn/tui.editor)  
[console.save](https://github.com/taurenshaman/console.save)  
