[...]


A script can be seem as the combination of small pieces of code. One kind of those pieces are the "objects". Let's understand how they work. 

Please, try this simple 5 steps exercise:

1. First, indentify some of the objects around you: your chair, your phone, a car.

2. Now, notice how each object has it's own set of characteristics. The car has a color, a brand, and a plate.

3. Also, notice that we can interect with each object in different ways: we can accelerate the car, or maybe wash it.

4. On the other hand, if you look at a FreePlane mindmap, you will see, for example, nodes, edges, icons. Those are objects inside FreePlane.

In the world of computer logic, the characteristics of an object are called "properties"; and the ways of interaction with the objects are called "methods". See this comparison between a real world object (let's say a person can be called, in computer logic, an "object") and a FreePlane object:

![image](https://user-images.githubusercontent.com/77707706/184511177-d6b4c5ba-9b82-46f3-a6c4-d65195de96dd.png)



[...]

//at this spot I will insert an explanation about how those elements are combined in expressions

[...]

Now, you may be thinking:

**Where can I find a list of Objects, Properties and Methods that exist in FreePlane, and that I can use in scripts?**

The simplest way to have an overview of those things, is looking in the  mindmap created when you navigate to the FreePlane menu option `Help->API Generator`.
There, you will find this list of types of objects:

![image](https://user-images.githubusercontent.com/77707706/184511226-5163459e-aa20-4b61-924c-c3f6908a1ed6.png)

Inside each one, you will find it's properties and methods. The properties have a wizard wand icon, and the methods have a star icon. For example, inside the Icons, you will find this:

![image](https://user-images.githubusercontent.com/77707706/184511248-9c3f4e2b-b475-40ed-a309-9367bde0abb1.png)

As an exercise, try to create some scripts using those methods that interact with Icons. After that, you can check an example of each of those methods in the following table:

| Method   | Example Script description                                                                                 | Example Script                                        |
| -------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| getAt    | If used on a node with 3 or more icons, it prints the 3rd icon name to the status bar                      | c.statusInfo = node.icons.getAt(2)                    |
| getFirst | Prints to the status bar the name of the first icon of the selected node                                   | c.statusInfo = node.icons.getFirst()                  |
| contains | Prints "true" to the status bar if the node has the "button\_ok" icon                                      | c.statusInfo = node.icons.contains("button\_ok")      |
| size     | Prints to the status bar the number of icons the selected node has                                         | c.statusInfo = node.icons.size()                      |
| getIcons | Prints to the status bar the number of icons the selected node has                                         | c.statusInfo = node.icons.getIcons()                  |
| getUrls  | Prints to the status bar the name of all the icons of the selected node                                    | c.statusInfo = node.icons.getUrls()                   |
| iterator | Prints to the status bar the name of all the icons of the selected node that have a name starting with "b" | c.statusInfo = node.icons.findAll{it.startsWith('b')} |
| add      | Adds the icon "button\_ok" to the selected node                                                            | node.icons.add("button\_ok")                          |
| addAll   |                                                                                                            |                                                       |
| addAll   | Finds all the nodes of the selected node, and add them again                                               | node.icons.addAll(node.icons.findAll())               |
| remove   | If used in a node with 3 or more icons, it removes the 3rd icon                                            | node.icons.remove(2)                                  |
| remove   | Removes the icon "button\_ok" from the selected node                                                       | node.icons.remove("button\_ok")                       |
| clear    | Removes all the icons from the selected node                                                               | node.icons.clear()                                    |

The most complete and updated list of objects, properties and methods is found at a place called API documentation, which can be opened by using that item of the menu: `Help->Freeplane API…`. Later, we will teach you how to navigate the API documentation.

