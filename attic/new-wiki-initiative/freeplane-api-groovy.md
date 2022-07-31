new-wiki-initiative
# Freeplane API Groovy tutorial

## Examples of each Method

| Interface                 | Method   | Example Script description                                                                                 | Example Script                                        |
| ------------------------- | -------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| org.freeplane.api.IconsRO | getAt    | If used on a node with 3 or more icons, it prints the 3rd icon name to the status bar                      | c.statusInfo = node.icons.getAt(2)                    |
| org.freeplane.api.IconsRO | getFirst | Prints to the status bar the name of the first icon of the selected node                                   | c.statusInfo = node.icons.getFirst()                  |
| org.freeplane.api.IconsRO | contains | Prints "true" to the status bar if the node has the "button\_ok" icon                                      | c.statusInfo = node.icons.contains("button\_ok")      |
| org.freeplane.api.IconsRO | size     | Prints to the status bar the number of icons the selected node has                                         | c.statusInfo = node.icons.size()                      |
| org.freeplane.api.IconsRO | getIcons | Prints to the status bar the number of icons the selected node has                                         | c.statusInfo = node.icons.getIcons()                  |
| org.freeplane.api.IconsRO | getUrls  | Prints to the status bar the name of all the icons of the selected node                                    | c.statusInfo = node.icons.getUrls()                   |
| org.freeplane.api.IconsRO | iterator | Prints to the status bar the name of all the icons of the selected node that have a name starting with "b" | c.statusInfo = node.icons.findAll{it.startsWith('b')} |
| org.freeplane.api.Icon    | add      | Adds the icon "button\_ok" to the selected node                                                            | node.icons.add("button\_ok")                          |
| org.freeplane.api.Icon    | addAll   |                                                                                                            |                                                       |
| org.freeplane.api.Icon    | addAll   | Finds all the nodes of the selected node, and add them again                                               | node.icons.addAll(node.icons.findAll())               |
| org.freeplane.api.Icon    | remove   | If used in a node with 3 or more icons, it removes the 3rd icon                                            | node.icons.remove(2)                                  |
| org.freeplane.api.Icon    | remove   | Removes the icon "button\_ok" from the selected node                                                       | node.icons.remove("button\_ok")                       |
| org.freeplane.api.Icon    | clear    | Removes all the icons from the selected node                                                               | node.icons.clear()                                    |
