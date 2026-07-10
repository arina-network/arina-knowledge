# Knowledge Processes Guide

## Atomic process

**Atomic process** can't be divided into subprocesses. Usually we use one sentences to describe it.

> System asks User to identify themselves.
 
> System informs User that authorization failed. 

> System identifies User.

## Flow process

**Flow process** can be divided into subprocesses that occur sequentially one after the other. 
Usually we use an ordered list to describe flow.

> 1. System asks User to identify themselves by Email
> 2. User enters Email and Password
> 3. System searches a User entity by Email and Password

## And process
**And process** is used for syntax simplification for a Flow process when subprocesses are short:

> System identifies User **and** informs User about new Subscription Plans **and** actual Marketing Actions  

## If process

**If process** describes checking some condition and executions only one of two subprocesses: the first subprocess for the valid condition and the second subprocess for the invalid condition.
Condition can be boolean expression or results of some process. Usually we use a `if-then-else` pattern with sublists.

> 1. System searches a User entity by Email and Password
> 2. **if** System found exactly one User entity
>     1. **then** System identifies User
>     2. **else** System informs User that authorization failed

## While process

**While process** describes repeating of subprocesses flow until some condition is met. 
Usually we use `while-Condition-do` pattern for checking condition **_before_** the execution of the flow, 
and `do-while-Condition` pattern for checking condition **_after_** the execution of the flow 

### while-Condition-do

> ### process Login
> 1. **while** there is no User Session for User 
>    1. System asks User to identify themselves.
>    2. User enters Email and Password
>    3. System authorizes User by Email and Password
>    4. **if** authorization was successful
>       1. **then** System creates User Session for User with State as Started  
>       2. **else**
>           1. System informs User that Email or Password is incorrect
>           2. **if** User decides to not continue
>               1. **then** fail

### do-while-Condition

> ### process Login
> 1. **do**
>    1. System asks User to identify themselves.
>    2. User enters Email and Password
>    3. System authorizes User by Email and Password
>    4. **if** authorization fails
>       1. **then**
>           1. System informs User that Email or Password is incorrect
>           2. **if** User decides to not continue
>               1. **then** fail
> 2. **while** System authorized User

## Repeat process

**Repeat process** describes repeating of subprocesses flow until it will be interrupted, but not more than max iterations. 
> 1. **repeat, max is 10**
>    1. System asks User to identify themselves.
>    2. User enters Email and Password
>    3. System authorizes User by Email and Password
>    4. **if** authorization was succeeded
>       1. **then** **complete**
>       2. **else**
>           1. System informs User that Email or Password is incorrect
>           2. **if** User decides to not continue
>               1. **then** fail
 
## For each process

**For each process** describes applying some subprocess for every item in list. Usually we use `for each-Entity-in-List` pattern.

> 1. **for each** Session **in** Active Session:
>     1. System finishes the Session 

## Complete, fail, error processes

**Complete, fail, error processes** are used for managing completion. 
By default, any process completes successfully exactly after the last subprocess in the process flow was finished.

We use `complete` when we need to successfully complete process in the middle of the flow.

> 1. **if** System found exactly one User entity
>     1. **then** **complete** 

We use `fail` when we need to fail process due to some logic in the middle of the flow.

> 1. **if** System found more than one User entity
>     1. **then** **fail** Two or more users were found 

We use `error` when we need to stop process because of some failure in the middle of the flow.

> 1. **if** Google Authentication Service returns timeout error
>     1. **then** **error** Google Authentication is not available 

## Create process

**Create process** describe creating an Entity. Usually we use `Actor-creates-Entity-with` pattern.

> 1. System **creates** User Session **with**:
>     - User **as** current User
>     - State **as** Started
>     - Started Time **as** now

## Modify process

**Modify process** describe changing attributes of an Entity. There are simple and detailed patterns.
Simple pattern is used when value is changed for one attribute (or few attributes) of entities, usually we use `set-Entity.Attribute-as-Value`.
Detailed - when values are changed for many attributes, usually we use `modify-Entity-set`.

### Simple modify process

> System **set** User Session.State **as** Finished

> System **set** User Session.State **as** Finished **and** Finished Time **as** now 
 
### Detailed modify process
> - System **modifies** User Session **set**:
>     - State **as** Finished
>     - Finished Time **as** now
>     - Finished by **as** System

## Destroy process

**Destroy process** describe destroying of an Entity or list of Entities. Usually we use `Actor-destorys-Entity` pattern.

> 1. System **destroys** User Session
 
> 1. System **destroys** all finished User Session which were finished more than 30 days ago

or

> 1. System **destroys** all User Session for which State is Finished **and** Finished Time is more than 30 days ago

## . process

**. process** is used for get attribute of entity. Can be applied recursivly if attribute has an entity type.

> Actor.Actor Type
 
> User Session.User.Actor.Actor Type

## Comparison processes

We use standard mathematical symbols `=`, `<>` or `!=`, `>`, `>=`, `<`, `<=` for do comparisions:
- `Value A = Value B`
- `Value A <> Value B` or `Value A != Value B`
- `Value A > Value B`
- `Value A >= Value B`
- `Value A < Value B`
- `Value A <= Value B`

Also, we can use `is` for comparing attribute with some value.

> 1. **if** User Session.State **is** Started
>    1. **then** **set** Session.State **as** Finished
>    2. **else** **fail** 

## Logic processes

We use `and`, `or` and `not` for boolean operations.

### and
> 1. **if** User Session.State **is** Started **and** User Session.Started Time **<** now - 30 days 
>    1. **then** **set** Session.State **as** Finished **and** User Session.Finished Time **as** now
>    2. **else** **fail** 

### or
 
> 1. **if** Actor.Actor Type **is** Human **or** Service
>    1. **then** System creates User Session
>    2. **else** **fail**

### not
> 1. **if** **not** Actor.Actor Type **is** Human
>    1. **then** **fail**

## In process

**In process** is used for checking if a value matches any value in a list.
> 1. **if** Actor.Actor Type **in** (Human, Service)
>    1. **then** System creates User Session
>    2. **else** **fail**

## Now process

**Now process** returns actual date and time.

> set Space.Created as **now**