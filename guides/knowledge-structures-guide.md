# Knowledge Structures Guide
_Author [Slava Zemlianskyi](https://www.linkedin.com/in/zemlianskyi/), published 2026-07-08 in [Arina Knowledge](https://github.com/arina-network/arina-knowledge)_

Formal model: [model Logic](/models/logic)

## Model

```
# model <Name>

## Overview
<Description>

## Actors
- [<Actor Name 1>](<local link>)
- ...

## Actor Stories
<Stories or link>

## Logical Data Structure

### Entities
- [<Entity Name 1>](<local link>)
- ...

### Categories
- [<Category Name 1>](<local link>)
- ...

### Constants
- [<Constant Name 1>](<local link>)
- ...

## Business Process Model

### <Process Group Name 1 >

- [<Process Name>](<local link>)
- ...

### <Process Group Name 2 >

- ...
```

## Actor

```
# actor <Name>
## description
<Description>
```

## Actor Story

```
# actor stories Pickups

## <Actor Stories Group Name 1 >

### actor story <Name>
**As** a <Actor Name>
**I want** <action or state description>
**So** <result description>
```

## Entity

```
# entity <Name>
## description
<Description>
## implements:
- [<Entity Name 1>](<link>)
...
## containers:
- [<Entity Name 1>](<link>)
...
## parts:
- [<Entity Name 1>](<link>) 
...
## attributes:
- <Attribute Name 1>, <Attribute type> or [<Entity Name 1>](<link>) 
- <Attribute Name 2>, list of <Attribute type> or [<Entity Name 1>](<link>) 
- <Attribute Name 3>, <Attribute type> or [<Entity Name 1>](<link>), required 
- <Attribute Name 4>, integer, min value is 0, max value is 100 
- <Attribute Name 5>, text, min length is 10, max length is 100 
- <Attribute Name 6>, text, length is 2, required 
```
[List of Data Types](/models/logic/data-types)

## Category

```
# category <Name>
## description
<Description>
## categories:
- <Category Name 1>
...

```

## Constant

```
# constant <Name>
## description
<Description>
## value
<Value>

```

## Process

```
# process <Name>
## description
<Description>

## actors:
- Name, [<Actor Name 1>](<link>) 
...

## inputs:
- <Input Name 1>, <Attribute type> or [<Entity Name 1>](<link>), required 
...

## outputs:
- <Output Name 1>, <Attribute type> or [<Entity Name 1>](<link>), required 
...

## flow
- <Step 1>
    - <Step 1.1>
    - ...
- if <Condition> 
    - then <Action 1>
    - else <Action 2>
- while <Condition>
    - do <Action>
- complete
- fail <Fail Information>
- error <Error Information>
- ...            

## acceptance criteria
### ac <Name>
**Given** <state 1>  
**and** <state 2>
**When** <action 1>  
**and** <action 2>
**Then** <result 1>   
**and** <result 2>
``` 
