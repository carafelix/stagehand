# stagehand
A typst template for easily creating pretty and legible theatre scripts meant for amateur use, with several useful gimmicks. This does not follow industry standards, but is meant to be easy to write, pleasing to the eye and highly customizable.

## Basic usage
If you just want to get started with the default values, simply init a new typst document with this template.
From the webapp, choose this template when starting a new project, from the CLI, use 
```bash
typst init @preview/stagehand:0.1.0
```
Read the template text to learn the basic syntax, and you're good to go!
I recommend setting aliases for recurring characters, and to use shorter, alternative function names, as shown in the template.

Alternatively, add this to the start of your typst file:
```typ
#import "@preview/stagehand:0.1.0":*
#show: theatre
```

## Features
Two different layouts: "fancy" and "concise".




### Functions
stagehand comes with the following functions:

#### speaker
Adds a speaker name. Arguments:
- name `(content)`: required
  - The name of the character
- t `(string|content|array(string|content)|auto|false)`: default: auto
  - With which character(s) to tag this line for the list of characters. Uses `name` by default. Doesn't tag this line at all if `false`
- p `(string|content)` default: none
  - If not none, adds a little stage direction directly behind the character name
 
#### stage-direction
Adds specially formatted stage directions. Arguments:
- body `(content)`: required
  - The content of the stage direction
- blocked `(boolean)`: default: false
  - If true, this is formatted as it's own block. If false, it is inline within other text.

#### prop
Marks text as a prop. It is not specially formatted, but will be listed and linked to in the prop section at the end of the file.

#### todo
Marks text as a TODO note. It will be brightly colored, and will be listed and linked to in the TODO section at the end of the file.


