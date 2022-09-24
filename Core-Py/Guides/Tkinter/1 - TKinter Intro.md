# TKinter Introduction
## _Overview of TKinter_
Stands for Tk-Interface, and is a library which contains distinct modules which allow for the development of a Python program which contains a user interface.

## Starting TKinter
Similar to the way that we have made use of other libraries in the past, Tkinter will use an import method to allow for use of its’ features.
```python
import tkinter as tk
```
When looking at online code, you may also come across the following:
```python
from tkinter import *
```
This will achieve a similar goal, however will remove the need for *tk.* to be used at the start of any Tkinter parts of your code, for the time being, we are going to focus on using *import tkinter as tk*.

On it's own, this will not do anything, however we will start looking at creating windows on our main screen.

## Creating a window
Creating windows within Tkinter requires and instance of Tkinters' tk to be called, depending upon the OS that is being used, the following will be created:
![Tkinter Windows](https://files.realpython.com/media/17_4_tk_window.662fec42e4f9.jpg)
```python
import tkinter as tk
window = tk.Tk()
```

Depending upon the IDE that you are using, you may need to add the following line at the end of the TKinter code in order to stop the program from "ending":

```python
import tkinter as tk
window = tk.Tk()
# Your other code will go here
window.mainloop()
```
This is your main structure that is used to initialise a TKinter front-end. We will work towards developing this further.