# digital-clock
from tkinter import*
from tkinter.ttk import*
from time import strftime

root =Tk()
root.title('clock')
def time():
    string = strftime('%H:%M:%S %P')
    lbl.config(text=string)
    lbl.after(1000,time)
lbl=label(root,font=('calibri',40,'bold'),
              background='red',foreground='white')
lbl.pack(anchor='center')
time()
mainloop()
