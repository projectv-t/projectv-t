# projectv-t

import math
import time 
import random
from tkinter import *
from buttons import *
def start():
    root = Tk()
    frame = Frame(root)
    root.overrideredirect(True)
    root.overrideredirect(False)
    root.attributes('-fullscreen', True)
    canva = Canvas(root, bg='white')
    canva.pack(fill=BOTH, expand=1)
    photo = PhotoImage(file="start_screen.png")
    screen_width = root.winfo_screenwidth()
    screen_height = root.winfo_screenheight()
    Label(root, image=photo).place(x=screen_width/2, y=screen_height/2, anchor="center")
    btn = Button(root, text="Start game", width=10, height=5, bg="#18ff95", fg="#ff182e", font="Arial 17")

    def deletescreen(event):
        root.destroy()
        rules()
    
    btn.bind("<Button-1>", deletescreen)
    btn.pack()
    root.mainloop()

def finish1():
    root = Tk()
    frame = Frame(root)
    root.overrideredirect(True)
    root.overrideredirect(False)
    root.attributes('-fullscreen', True)
    canva = Canvas(root, bg='black')
    canva.pack(fill=BOTH, expand=1)
    photo = PhotoImage(file="win_0.png")
    screen_width = root.winfo_screenwidth()
    screen_height = root.winfo_screenheight()
    Label(root, image=photo).place(x=screen_width/2, y=screen_height/2, anchor="center")
    btn = Button(root, text="Again", width=10, height=2, bg="#18ff95", fg="#ff182e", font="Arial 17")

    def deletescreen(event):
        root.destroy()

    btn.bind("<Button-1>", deletescreen)
    btn.pack()
    root.mainloop()

def finish2():
    root = Tk()
    frame = Frame(root)
    root.overrideredirect(True)
    root.overrideredirect(False)
    root.attributes('-fullscreen', True)
    canva = Canvas(root, bg='black')
    canva.pack(fill=BOTH, expand=1)
    photo = PhotoImage(file="win_x.png")
    screen_width = root.winfo_screenwidth()
    screen_height = root.winfo_screenheight()
    Label(root, image=photo).place(x=screen_width/2, y=screen_height/2, anchor="center")
    btn = Button(root, text="Again", width=10, height=2, bg="#18ff95", fg="#ff182e", font="Arial 17")

    def deletescreen(event):
        root.destroy()

    btn.bind("<Button-1>", deletescreen)
    btn.pack()
    root.mainloop()

def finish3():
    root = Tk()
    frame = Frame(root)
    root.overrideredirect(True)
    root.overrideredirect(False)
    root.attributes('-fullscreen', True)
    canva = Canvas(root, bg='black')
    canva.pack(fill=BOTH, expand=1)
    photo = PhotoImage(file="drawn.png")
    screen_width = root.winfo_screenwidth()
    screen_height = root.winfo_screenheight()
    Label(root, image=photo).place(x=screen_width/2, y=screen_height/2, anchor="center")
    btn = Button(root, text="Again", width=10, height=2, bg="#18ff95", fg="#ff182e", font="Arial 17")

    def deletescreen(event):
        root.destroy()

    btn.bind("<Button-1>", deletescreen)
    btn.pack()
    root.mainloop()
    
def rules():
    root = Tk()
    frame = Frame(root)
    root.overrideredirect(True)
    root.overrideredirect(False)
    root.attributes('-fullscreen', True)
    canva = Canvas(root, bg='white')
    canva.pack(fill=BOTH, expand=1)
    screen_width = root.winfo_screenwidth()
    screen_height = root.winfo_screenheight()
    photo = PhotoImage(file="button_1.png")
    lable1 = Label(text="Правила", font="Arial 30", bg="white", fg="#ff182e").place(x=600, y=50)
    lable2 = Label(text="Игроки по очереди ставят на свободные клетки поля 3х3 знаки\n (один всегда крестики, другой всегда нолики).\n Первый, выстроивший в ряд 3 своих фигуры по вертикали,\n горизонтали или диагонали, выигрывает. \n Первый ход делает игрок, ставящий крестики.", font="Arial 25", justify=CENTER, bg="white").place(x=700, y=300, anchor="center")
    btn = Button(root, image=photo)
    
    def deletescreen(event):
        root.destroy()
        buttons()
        
    btn.bind("<Button-1>", deletescreen)
    btn.pack()
    root.mainloop()

start()
