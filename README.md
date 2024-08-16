import tkinter as tk
from time import strftime

# Função para atualizar o tempo
def time():
    string = strftime('%H:%M:%S')  # Formato de 24 horas (HH:MM:SS)
    label.config(text=string)  # Atualiza o texto do rótulo com o tempo atual
    label.after(1000, time)  # Atualiza a cada 1000 milissegundos (1 segundo)

# Configuração da janela principal
root = tk.Tk()
root.title('Relógio Digital')  # Título da janela

# Configuração do rótulo do relógio
label = tk.Label(root, font=('calibri', 40, 'bold'), background='black', foreground='white')
label.pack(anchor='center')

time()  # Chama a função de tempo para iniciar o relógio

root.mainloop()  # Mantém a janela aberta

# JustAClock
