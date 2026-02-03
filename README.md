import tkinter as tk
from tkinter import font

root = tk.Tk()
root.title("Проєкт з полем і кнопкою")
root.geometry("400x250")

arial_font = font.Font(family="Arial", size=10)

entry = tk.Entry(
    root,
    width=15,
    bd=3,
    font=arial_font
)

entry.pack(pady=(30, 10))

def on_click():
    entry.config(
        bg="red",
        fg="white",
        font=("Arial", 14)
    )
    
    entry.config(width=35)
    
    entry.delete(0, tk.END)
    entry.insert(0, "Ми використовуємо властивості поля!")

button = tk.Button(
    root,
    text="8-Б",
    width=10,
    fg="blue",
    bg="yellow",
    command=on_click
)

button.pack()

root.mainloop()
