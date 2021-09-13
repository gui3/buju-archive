# App development roadmap

Everything about coding the app

### done

- choose a framework (react native)

### todo

- code the app

===

## brainstorm

name : buju for bullet journal

### components & features

everything is an entry


#### ENTRIES

- title* str
- label* str (automatic with _ replacers for spaces/#/@ and increment)
- color* str (hex, default ffffff)
- description str
- priority* int (default 0, flagged -1)
- tags str (automatic from description with #tags)?
- parent* str (root parent = "_" if none)
- checkable bool
- datecreation* date (automatic)
- dateupdate* date (automatic)
- datestart date
- dateend date
- datechecked date
- type int

---
Types of entries (compulsory* fields always present) :

- 0 **tag :** 
  title, description, priority, tags; 
  only meant to categorize 

- 1 **note :** 
  title, description, priority, tags, datestart; 
  a note about anything 

- 2 **task :** 
  all fields & checkable = true; 

- 4 **list :** 
  title, description, priority, tags, checkable = false; 
  has a button to add items to it 

- 5 **item :** 
  title, checkable = true; 
  the simplest entry, cannot have children nor tags 
  visually attached to its parent 

- 6 **page :** (to be coded later) 
  title, description, priority, tags; 
  a long page where you can write in markdown
  & insert other entries (@tag)
  OR insert searches (#@tag)


#### VIEWS

- **chrono view :** 
  modes : PLANNING, HISTORY, MIXED

- **task view :** 
  tabs : UNDONE, DONE, OTHER

- **tags view :** 
  modes : TAGS ONLY, ALL
  show only title and number of references

- **tree view :** 
  show hierarchically by parents

