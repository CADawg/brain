---
dg-publish: true
---
`*` Marks the place where you need to have your cursor parked in order to use that feature.

Most of this is taken from the [IDE Features Trainer](https://plugins.jetbrains.com/plugin/8554-ide-features-trainer) Plugin and is an incomplete list.

- **CTRL + SPACE**
  - Show Suggestions
- **ALT + ENTER**
  - Show Intentions
	  - ``` `json*:"fieldName"` ``` -> Change field name style = Change field casing
	  - ``` `json*:"fieldName"` ``` -> Update all key value in tags at once. (Add ,omitempty)
	  - ``` `json*:"fieldName"` ``` -> Add keys to tags (generate new tags like db)
	  - `*struct` -> Generate struct tags from JSON (Paste in JSON)
	  - `func y(*thingOne string, thingTwo string)` -> Reformat Arguments
- **Double Tap Shift**
  - Search Everywhere
- **Ctrl + Q**
  - View Quick Documentation
	  - Twice to open sidebar
- **F2**
  - Go to next error in file
- **Function -> Right Click -> Generate... -> Tests**
  - Generate Tests for Function
- **Ctrl + Shift + A**
  - Search Everywhere (Actions only)
	  - Turn on Soft Wraps For File
- **Ctrl + Shift + ->**
  - Highlight next code block
- **Ctrl + W**
  - Extend selection to next code block
  - (+ Shift = Shrink Selection)
- **Ctrl + /**
  - Comment out line
- **Ctrl + Shift + /**
  - Comment selection
- **Paste in JSON (Dialog Pops Up)**
  - Convert to go Struct
- **Escape on generated text**
  - Finish editing
- **Ctrl + Alt + Shift + T**
  - Extract Type
- **Ctrl + Shift + Enter**
  - Complete statement and newline