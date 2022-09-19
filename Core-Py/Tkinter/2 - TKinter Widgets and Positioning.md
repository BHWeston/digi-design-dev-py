# Tkinter Widgets Intro and Positioning
Previously having looked at creating the basic structure of a Tkinter window, using the below, let's now look at adding different elements onto our interface window:
```python
import tkinter as tk
window = tk.Tk()
# Your other code will go here
window.mainloop()
```
## Widgets
Prior to looking at creating outputs within a Tkinter window, we need to understand the idea of *widgets* within the Tk library. Widgets are GUI (graphical user interface) elements that we can add onto the screen, this includes but is not limited to:
- Label
- Button
- Entry
- Radiobutton
- Text
- Option

This document will focus on some of the outputs that we can have within Tkinter:
## Labels
Adding in a label within Tkinter will make use of a *Label()* method, this will look like the following:
```python
import tkinter as tk
window = tk.Tk()
label = tk.Label()
window.mainloop()
```
The *Label()* method will take a variety of arguments, this includes *text, width, pady, wraplength, bg and font*. Let's have a look at some of these and implement this within our program. Further details around the arguments that we can add can be found here [Tkinter Label](https://www.tutorialspoint.com/python/tk_label.htm):
```python
import tkinter as tk
window = tk.Tk()
label = tk.Label(text = "Example")
window.mainloop()
```
On it's own, this will only create an instance of a *Label* with the text of "Example" inside of it. If we are wanting to place this on the screen, there are three different ways in which we can do so:
- place() 
- pack()
- grid()

These are what are known as **geometry managers**. Here is a comparison between them:
![Pack vs. Grid vs. Place](http://gatherworkshops.github.io/programming/courses/tkinter/assets/images/geometry-managers.svg)
Let's go through each of these in detail:
### pack()
The easiest option that we can look at using within Tkinter. This will position the element in relation to other elements on the screen, for instance:
```python
import tkinter as tk

window = tk.Tk()
label = tk.Label(text = "Example")
label.pack()
window.mainloop()
```
This will add "Example" onto our Tk window. If we wanted to add some more text onto this, it would look like the following:
```python
import tkinter as tk

window = tk.Tk()
label = tk.Label(text = "Example")
label.pack()

moreText = tk.Label(text="Other Text")
moreText.pack()
window.mainloop()
```
This will add the "Other Text" information directly underneath the "Example" element. Consider this similar to when you create multiple *<div>* elements within your HTML work.
As detailed within the following link from tutorialspoint, [TutorialsPoint - pack()](https://www.tutorialspoint.com/python/tk_pack.htm) can take the following arguments:
- expand: This will fill space not used by a parent element (more on this within future documents)
- fill: This will fill extra space on an axis that you define e.g. *fill = tk.X* will will the data horizontally. More on this when we look at input widgets.
- side: Will change the position of text on screen, let's look at how this functions.

##### side
This will change the position of the text displayed on the screen. the sytnax looks like the following:
> side = tk.BOTTOM
side = tk.TOP
side = tk.LEFT
side = tk.RIGHT

Using these within the *Label()* method will allow for content to be positioned differently on the screen, for instance:
```python
import tkinter as tk

window = tk.Tk()
label = tk.Label(text = "Example")
label.pack(side = tk.BOTTOM)

moreText = tk.Label(text="Other Text")
moreText.pack(side = tk.TOP)
window.mainloop()
```
This will move the "Other Text" to the top of the screen, with "Example" now being moved to the bottom. This will allow for text to be organised in specific positions.

There is a limitation with this type of geometry manager however, as this will not allow for specific placement of elements. This is where *place()* and *grid()* come in.

### place()
Similar to the way in which you would traditionally position elements within website development (specifically CSS), you can use *place()* to position elements in an exact pixel position. This will make use of some of the many arguments that you can add within the *place()* method, this includes (but is not limited to):
- Height
- Width
- relx
- rely
- x
- y

Further details on each of these can be found within the Tkinter documentation, you can also find the full list on tutorialspoint here: [TutorialsPoint - place()](https://www.tutorialspoint.com/python/tk_place.htm).

The below example looks at moving an element to a specific X and Y co-ordinate:
```python
import tkinter as tk

window = tk.Tk()
label = tk.Label(text = "Example")
label.place(x = 50, y = 50)
window.mainloop()
```

> Experiment with the other arguments that you can add into the *place()* method to see how they all differ.

### grid()
Used within website development frameworks such as Bootstrap, you will look at using grid systems to position elements on the screen. Tkinter allows for you to position elements in a similar style. See the diagram:
![Grid Geometry](https://www.pythontutorial.net/wp-content/uploads/2021/01/Tkinter-grid-Grid-Geometry.png)

The *grid()* method allows for you to position elements in a similar format, for instance:
```python
import tkinter as tk

window = tk.Tk()
label = tk.Label(text = "Example")
label.grid(column = 0, row = 0)

anotherLabel = tk.Label(text = "Other Text")
anotherLabel.grid(column = 2, row = 1)
window.mainloop()
```

Be aware that by default, the sizing of the columns and rows are based upon what is inside those boxes. For instance, if you were to change *anotherLabel* from above to column = 3, it will still look like it is within column 2, due to there being nothing within column 2 to space out the content.

This is why you can also use commands such as:
- rowspan
- columnspan
- ipadx
- ipady
- padx
- pady
- sticky

> Experiment with these and see how they function within this method. An example image has been provided below:

![Span of Cols and Rows](https://www.pythontutorial.net/wp-content/uploads/2021/01/Tkinter-grid-columnspan-rowspan.png)

We will experiment with all of these through-out the coming weeks.