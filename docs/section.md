# Section | 部件 | 片段

A section is a card with front and back content.

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

## Front Card
```json
{
    "front": {
        "content": "{markdown}"
    }
}
```

## Back Card
```json
{
    "back": {
        "content": "{markdown}"
    }
}
```

## Tech Stack
Web Frontend:  
[tui.editor](https://github.com/nhn/tui.editor)  
FlipCard of Metro, instead of ~~[jquery.flip](https://github.com/nnattawat/flip)~~.