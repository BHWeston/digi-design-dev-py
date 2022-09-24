# Tkinter Styling
This section will focus on the styling techniques that can be done using Tkinter. We are going to start with the following code and build up from there:
```python
import tkinter as tk

window = tk.Tk()
label = tk.Label(text = "Example")
label.grid(column = 0, row = 0)
window.mainloop()
```
## Title
By default when running on a Windows OS, at the top left of your created window, you will have a feather with the words "tk" after. This will look something like the following:
![Tkinter Default Window](https://www.pythontutorial.net/wp-content/uploads/2020/11/Tkinter-window-default.png)

We are able to modify this by using the *title()* method. For this, we are going to want to modify the window that we have created, with the syntax looking like the following:
```python
window.title("New Title")
```
If we were to add this to our initial code, it would look something like this:
```python
import tkinter as 
window = tk.Tk()

# Adds a title to our interface
window.title("New Title")

label = tk.Label(text = "Example")
label.grid(column = 0, row = 0)
window.mainloop()
```

> Note that you may need to resize the window in order to be able to see this. If we want Tkinter to do this for us, we can use the *geometry* command.

## Geometry
As mentioned within the previous section, this will look at changing the size of a window with Tkinter. The syntax for this is as follows:
```python
window.geometry("400x400")
```
This will change the dimensions of the screen. 

## Colours (bg and fg)
There will be times where you will want to style your Tkinter interface with colours. We can use either of the following to do this:
- fg = Foreground
- bg = Background

Let's say that we wanted to change the background colour of the window to blue, the syntax would look like the following:
```python
window["bg"] = "blue"
```
This will change the colour to look like the following:
![Window with background colour of blue](https://www.delftstack.com/img/Tkinter/Tkinter%20set%20background%20color%20-%20bg%20attribute.png?ezimgfmt=rs:302x232/rscb5/ng:webp/ngcb5)
There are many different colours that are built-in, this includes the following:
![Background colours](http://knowpapa.com/wp-content/uploads/2018/01/tkcolors.png)

This same concept can be done with labels and other elements provided, for instance, the below will change the text colour to orange:
```python
label["fg"] = "orange"
```

Putting all of this together, we can create a blue background with some orange text:
```python
import tkinter as tk

# Window Details #
window = tk.Tk()

window.title("New Title")
window.geometry('400x400')
window["bg"] = "blue"

# Label Details #
label = tk.Label(text = "Example")
label["fg"] = "orange"
label.grid(column = 0, row = 0)

window.mainloop()
```

> Consider any issues with the output provide from the above, think about what you would change for this.