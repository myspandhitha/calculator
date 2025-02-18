# calculator
from tkinter import *

root = Tk()

root.title("Calculator")
root.configure(background="#808080")  # Dark grey background

e = Entry(
    root,
    width=35,
    borderwidth=5,
    background="white"
    )
e.grid(
    row=0,
    column=0,
    columnspan=3,
    padx=10,
    pady=10
    )

def button_click(number):
    current = e.get()
    e.delete(0, END)
    e.insert(0, str(current) + str(number))

def button_clear():
    e.delete(0, END)

def button_add():
    first_number = e.get()
    global f_num
    global math
    math = "addition"
    f_num = int(first_number)
    e.delete(0, END)

def button_equal():
    second_number = e.get()
    e.delete(0, END)
    if math == "addition":
        e.insert(0, f_num + int(second_number))
    if math == "subtraction":
        e.insert(0, f_num - int(second_number))
    if math == "multiplication":
        e.insert(0, f_num * int(second_number))
    if math == "division":
        e.insert(0, f_num / int(second_number))

def button_subtract():
    first_number = e.get()
    global f_num
    global math
    math = "subtraction"
    f_num = int(first_number)
    e.delete(0, END)

def button_multiply():
    first_number = e.get()
    global f_num
    global math
    math = "multiplication"
    f_num = int(first_number)
    e.delete(0, END)

def button_divide():
    first_number = e.get()
    global f_num
    global math
    math = "division"
    f_num = int(first_number)
    e.delete(0, END)

# Make buttons
button1 = Button(
    root,
    text="1",
    padx=30,
    pady=20,
    command=lambda: button_click(1),
    bg="#DCDCDC",  # Light grey
    fg="black"
)
button2 = Button(
    root,
    text="2",
    padx=30,
    pady=20,
    command=lambda: button_click(2),
    bg="#DCDCDC",
    fg="black"
)
button3 = Button(
    root,
    text="3",
    padx=30,
    pady=20,
    command=lambda: button_click(3),
    bg="#DCDCDC",
    fg="black"
)
button4 = Button(
    root,
    text="4",
    padx=30,
    pady=20,
    command=lambda: button_click(4),
    bg="#DCDCDC",
    fg="black"
)
button5 = Button(
    root,
    text="5",
    padx=30,
    pady=20,
    command=lambda: button_click(5),
    bg="#DCDCDC",
    fg="black"
)
button6 = Button(
    root,
    text="6",
    padx=30,
    pady=20,
    command=lambda: button_click(6),
    bg="#DCDCDC",
    fg="black"
)
button7 = Button(
    root,
    text="7",
    padx=30,
    pady=20,
    command=lambda: button_click(7),
    bg="#DCDCDC",
    fg="black"
)
button8 = Button(
    root,
    text="8",
    padx=30,
    pady=20,
    command=lambda: button_click(8),
    bg="#DCDCDC",
    fg="black"
)
button9 = Button(
    root,
    text="9",
    padx=30,
    pady=20,
    command=lambda: button_click(9),
    bg="#DCDCDC",
    fg="black"
)
button0 = Button(
    root,
    text="0",
    padx=30,
    pady=20,
    command=lambda: button_click(0),
    bg="#DCDCDC",
    fg="black"
)
button_add = Button(
    root,
    text="+",
    padx=30,
    pady=20,
    command=button_add,
    bg="#DCDCDC",
    fg="black"
)
button_equal = Button(
        root,
    text="=",
    padx=68,
    pady=20,
    command=button_equal,
    bg="#DCDCDC",
    fg="black"
)
button_clear = Button(
    root,
    text="Clear",
    padx=58,
    pady=20,
    command=button_clear,
    bg="#DCDCDC",
    fg="black"
)

button_subtract = Button(
    root,
    text="-",
    padx=30,
    pady=20,
    command=button_subtract,
    bg="#DCDCDC",
    fg="black"
)
button_multiply = Button(
    root,
    text="*",
    padx=30,
    pady=20,
    command=button_multiply,
    bg="#DCDCDC",
    fg="black"
)
button_divide = Button(
    root,
    text="/",
    padx=30,
    pady=20,
    command=button_divide,
    bg="#DCDCDC",
    fg="black"
)


# Put buttons on screen
button1.grid(row=3, column=0)
button2.grid(row=3, column=1)
button3.grid(row=3, column=2)
button4.grid(row=2, column=0)
button5.grid(row=2, column=1)
button6.grid(row=2, column=2)
button7.grid(row=1, column=0)
button8.grid(row=1, column=1)
button9.grid(row=1, column=2)
button0.grid(row=4, column=0)
button_add.grid(row=5, column=0)
button_equal.grid(row=5, column=1, columnspan=2)
button_clear.grid(row=4, column=1, columnspan=2)
button_subtract.grid(row=6, column=0)
button_multiply.grid(row=6, column=1)
button_divide.grid(row=6, column=2)

root.mainloop()
