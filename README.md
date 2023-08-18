This repository is a collection of notes for [Illumination Engine](https://github.com/PercentBoat4164/Illumination-Engine). 

# Recommended plugins
* Dataview - Michael Brenan
* Kanban - mgmeyers
* Calender - Liam Cain
* Obsidian Git 

# Todo List - Today
```dataview 
TASK FROM #todo WHERE !completed AND due
```
# Todo List - General

```dataview
TASK FROM #todo AND "General Conifer" WHERE !completion SORT file ASC
```
# Todo List - DLSS
```dataview
TASK FROM "DLSS Plugin" WHERE !completion SORT file ASC
```


# Recently Completed Tasks
```dataview
TASK FROM #todo AND !"Illumination Engine"
WHERE completion
SORT completion DESC
```