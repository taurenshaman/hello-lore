# LanguagePack | 语言学习卡片包
Cards pack for language learning.

## Context
```json
{
    "context": {
        "title": "{title}",
        "uri": "{uri}",
        "description": "{markdown}"
    }
}
```

## Data
```json
{
    "language": "en",
    "items": [
        // item type: vocabulary
        // id and author are both NULL
        {
            "id": null,
            "type": "language:vocabulary",
            "author": null,
            "title": "cat",
            "description": "",
            "descriptionType": "markdown",
            "images": [ // Optional. 9 images got from Bing Image Search.
            ]
        },
        // item type: note (Lore)
        // The note is indicated by id, type and author.
        // "title" is like a cache, which will not be updated automatically.
        {
            "id": "b51f46f41f894c9a9d43859a756ef1b7",
            "type": "dialog",
            "author": "jerin",
            "title": "对话: 2019/11/25"
        },
        {
            "id": "d5aa9d79566d4469bf22c116a1a212a6",
            "type": "section",
            "author": "jerin",
            "title": "灵魂的转生与新生"
        },
    ]
}
```