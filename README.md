# Password_Generator
Password Generator made in Python.
                                                  CODE :
                                                  ______________
                                                  
                                                  
from tkinter import *
from tkinter import messagebox
from tkinter.ttk import *
import random
from pprint import pprint

root = Tk()
root.title("Login")
root.geometry("600x400")
root.resizable(width=False, height=False)


usuario = Label(root, text="ingrese nombre de usuario")
usuario.pack()

usuario1 = StringVar()
usu = Entry(root, width=30, textvariable=usuario1)
usu.pack()


def ingresar():
    minus = "qwertyuiopasdfghjklzxcvbnm"
    mayus = minus.upper()
    numeros = "0123456789"
    simbolos = "!%&/()=[]}{-.,_:#"
    inputFile = 'data.txt'

    base = minus + mayus + numeros + simbolos
    longitud = 12


    for _ in range(1):
        muestra = random.sample(base, longitud)
        password = "".join(muestra)
        getUsuario = str(usuario1.get() + ' ; ' + password)  
    f = open (inputFile, 'a')
    f.write('\n' + getUsuario)
    f.close()
    with open(inputFile, "r") as f1:
        last_line = f1.readlines()[-1]

        
    if last_line == getUsuario:
        messagebox.showinfo("Estado", "Contraseña Guardada")
    else:
        messagebox.showerror("Error", )    



bt = Button(root, text="Generar contraseña", command=ingresar)
bt.pack(side=BOTTOM)
root.mainloop()                                           
