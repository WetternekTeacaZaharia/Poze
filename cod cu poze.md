# Poze
Perspectivă poze jucator si pc
from tkinter import *
#main fereastra
root= Tk()
root.title("Rock Scissors Paper")                                   #titlu fereastra
root.configure(background= "purple")

#pentru poze (instalare pip in terminal)
piatra_img = ImageTk.PhotoImage(Image.open("piatra.png"))
hartie_img = ImageTk.PhotoImage(Image.open("hartie.png"))
foarfeca_img = ImageTk.PhotoImage(Image.open("foarfeca.png"))

#poze prima perspectiva(mai un set de 3 poze pt perspectiva2)
piatra_img_comp = ImageTk.PhotoImage(Image.open("piatra_2.png"))
hartie_img_comp = ImageTk.PhotoImage(Image.open("hartie_2.png"))
foarfeca_img_comp = ImageTk.PhotoImage(Image.open("foarfeca_2.png"))

#etichetele
user_indicator = Label(root, font=50, text ="EU",bg="purple", fg="white")
computer_indicator = Label(root, font=50, text="COMPUTER",bg="purple", fg="white")
user_indicator.grid(row=0 , column=3 )
computer_indicator.grid(row=0 , column=1 )

#####pt sccor
jucatorScor = Label(root,text =0, font =100,bg="purple", fg="white")
computerScor = Label(root, text=0,font =100,bg="purple", fg="white" )
computerScor.grid(row=1,column=1)
jucatorScor.grid(row=1,column=3)
#mesajele
mesaje = Label(root,font =50, bg="purple", fg="white")                     #, text = "Ai pierdut!")
mesaje.grid(row=3, column=2)

#actualizarea mesajului
def actualiz_Mesaj(x):
    mesaje ['text'] = x

#actualizarea scorului meu

def actualiz_Iscor():                                                       #scorul jucatorului
     scor = int(jucatorScor["text"])
     scor = scor+ 1
     jucatorScor["text"] = str(scor)


root.mainloop()
