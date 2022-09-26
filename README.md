from tkinter import *

from tkinter import ttk as ttkz
#Ventana Principal
ventana =Tk()
ventana.title("PRINCIPAL")

def login():
    if usuario.get()=="ivan" and contraseña.get()=="ivan":
        principal()
#Fram
def principal():
    principal =Tk()
    principal.title("Empresa de Transportes LA LIEBRE")
    
    principalFrame =Frame(principal)
    principalFrame.pack()
    principalFrame.config(width=300, height=300,background = "#213141")
    
    #TituloLabel
    lbltitulo =Label(principalFrame, text="Transportes La Liebre",
               font=("Arial",20))
    lbltitulo.grid(column=0,row=0,padx=10,pady=10,columnspan=2)
    
    #TextoFechaViaje
    lbl_fecha = Label(principalFrame, text="Seleccionar Fecha de Viaje:")
    lbl_fecha.grid(column =0 , row = 1,ipadx=2,ipady=2,padx=5,pady=5)
    lbl_fecha1 = Label(principalFrame, text="Seleccionar Fecha de Viaje2:")
    lbl_fecha1.grid(column =1 , row = 1,ipadx=2,ipady=2)
    lbl_fecha2 = Label(principalFrame, text="Seleccionar Fecha de Viaje3:")
    lbl_fecha2.grid(column =0 , row = 3,ipadx=2,ipady=2)
    
def loginMenu():
    loginFrame =Frame(ventana)
    loginFrame.pack()
    loginFrame.config(width=200, height=200,background = "#213141")
    
    #TituloLabel
    lbl =Label(loginFrame,background="lightblue", text="Transportes La Liebre",
               font=("Arial",20))
    lbl.grid(column=0,row=0,padx=10,pady=10,columnspan=2)
    
    #TextoUsuario
    usuario = StringVar()
    usuario.set("Inserte Usuario")      # se crea la variable para la caja de texto del usuario con StringVar
    usuariotxt = ttk.Entry(loginFrame,textvariable=usuario, font=("Time New Roman",10))
    usuariotxt.grid(column=0,row=1,padx=10,pady=10,columnspan=2)
    #TextoContraseña
    contraseña = StringVar()
    contraseña.set("Inserte Contraseña")      # se crea la variable para la caja de texto del usuario con StringVar
    contraseñatxt = ttk.Entry(loginFrame,textvariable=contraseña,show="*", font=("Time New Roman",10))
    contraseñatxt.grid(column=0,row=2,padx=10,pady=10,columnspan=2)
    #BotonAceptar
    btn_ingresar =ttk.Button(loginFrame,text="INGRESAR", command=principal)
    btn_ingresar.grid(column=0,row=3,pady=10)
    
    
    btn_salir =ttk.Button(loginFrame,text="SALIR")
    btn_salir.grid(column=1,row=3,pady=10)
loginMenu()
ventana.mainloop()
