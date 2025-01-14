import tkinter as tk
from tkinter import messagebox, simpledialog
import random

# Lista inițială de idei
idei = [
    "Creează un site web personal.",
    "Începe un jurnal de călătorie.",
    "Construiește un robot simplu.",
    "Creează o aplicație mobilă.",
    "Învață să cânți la un instrument nou.",
    "Scrie o poveste scurtă.",
    "Pictează o operă de artă.",
    "Explorează fotografia de natură.",
    "Construiește un joc video simplu.",
    "Începe un vlog pe YouTube."
    "Organizează un maraton de citit cărți.",
    "Construiește o casă pentru păsări.",
    "Creează un podcast pe un subiect care te pasionează.",
    "Învață să gătești un preparat exotic.",
    "Plantează o grădină de plante aromatice.",
    "Proiectează un design pentru tricouri personalizate.",
    "Explorează scrierea caligrafică sau lettering-ul artistic.",
    "Învață să editezi videoclipuri profesionist.",
    "Construiește o aplicație pentru organizarea timpului.",
    "Creează un album foto tematic (de exemplu, „locuri preferate”)."
]

# Lista pentru ideile salvate
idei_salvate = []

def genereaza_idee():
    """Funcție pentru generarea aleatorie a unei idei."""
    if idei:
        idee = random.choice(idei)
        eticheta_idee.config(text=idee)
    else:
        eticheta_idee.config(text="Nu mai există idei disponibile.")

def salveaza_idee():
    """Funcție pentru salvarea ideii curente."""
    idee = eticheta_idee.cget("text")
    if idee and idee not in idei_salvate:
        idei_salvate.append(idee)
        messagebox.showinfo("Salvare", "Ideea a fost salvată cu succes!")
    elif idee in idei_salvate:
        messagebox.showwarning("Avertizare", "Această idee a fost deja salvată.")
    else:
        messagebox.showerror("Eroare", "Nu există nicio idee de salvat.")

def adauga_idee():
    """Funcție pentru adăugarea unei idei noi în listă."""
    idee_noua = simpledialog.askstring("Adaugă idee", "Introdu ideea ta:")
    if idee_noua:
        idei.append(idee_noua)
        messagebox.showinfo("Succes", "Ideea a fost adăugată cu succes!")
    else:
        messagebox.showwarning("Avertizare", "Nu s-a introdus nicio idee.")

def vezi_idei_salvate():
    """Funcție pentru afișarea ideilor salvate."""
    if idei_salvate:
        mesaj = "\n".join(idei_salvate)
        messagebox.showinfo("Idei Salvate", mesaj)
    else:
        messagebox.showinfo("Idei Salvate", "Nu există idei salvate.")

# Configurarea ferestrei principale
fereastra = tk.Tk()
fereastra.title("Generator de Idei Creative")
fereastra.geometry("500x400")
fereastra.resizable(False, False)

# Eticheta principală pentru afișarea ideii generate
eticheta_idee = tk.Label(fereastra, text="Apasă pe 'Generează Idei' pentru a începe!",
                         wraplength=400, font=("Arial", 14), justify="center")
eticheta_idee.pack(pady=20)

# Buton pentru generarea unei idei
buton_genereaza = tk.Button(fereastra, text="Generează Idei", font=("Arial", 12), command=genereaza_idee)
buton_genereaza.pack(pady=10)

# Buton pentru salvarea ideii
buton_salveaza = tk.Button(fereastra, text="Salvează Ideea", font=("Arial", 12), command=salveaza_idee)
buton_salveaza.pack(pady=10)

# Buton pentru adăugarea unei idei noi
buton_adauga = tk.Button(fereastra, text="Adaugă Idee Nouă", font=("Arial", 12), command=adauga_idee)
buton_adauga.pack(pady=10)

# Buton pentru vizualizarea ideilor salvate
buton_vezi_salvate = tk.Button(fereastra, text="Vezi Ideile Salvate", font=("Arial", 12), command=vezi_idei_salvate)
buton_vezi_salvate.pack(pady=10)

# Rulare aplicație
fereastra.mainloop()
