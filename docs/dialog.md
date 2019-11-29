# Dialog | Chat flow | 对话

A dialog is group of chat contents.

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

## Participants
```json
agents: [
    {
        "id": "agent_3",
        "name": "成天乐",
        "title": "",
        "avatarType": "robot", // will be supporte in future
        "semantics": [] // will be supporte in future
    },
]
```

## Dialog Item
```json
items: [
    {
        "id": "chat_item_1",
        "time": "Fri, 22 Nov 2019 15:35:17 GMT",
        "position": "left", // left/right
        "text": "老白啊，你听课就不能认真点？",
        "agentId": "agent_3",
        "delay": 1, // will be supporte in future
        "precedingAside": "some aside, then dialog happened.",
        "followingAside": "some aside after dialog"
    },
]
```

## Tech Stack
Web Frontend:  
[tui.editor](https://github.com/nhn/tui.editor)  
[Ractive](https://ractive.js.org)