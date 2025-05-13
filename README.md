🧠 Contador de Palavras com Interface Gráfica
Esse projeto é uma aplicação simples feita com Tkinter e Matplotlib, que conta a frequência de palavras em um texto e exibe os resultados em um gráfico de barras.

💡 Funcionalidades
Interface gráfica para digitar ou colar o texto.

Contagem de palavras ignorando maiúsculas/minúsculas e vírgulas.

Geração de gráfico com a frequência de cada palavra.

📸 Interface
Ao iniciar, você verá:

Um campo de texto para entrada.

Um botão “Contar Palavras”.

Uma janela popup com o gráfico gerado automaticamente.

🧩 Código-fonte principal
python
Copiar
Editar
from tkinter import Tk, Label, Text, Button
import matplotlib.pyplot as plt

def contar_palavras():
    lista_texto = texto.get('1.0', 'end-1c').replace(",", " ").lower().split()
    resultado = lambda x: lista_texto.count(x)
    palavras = map(resultado, lista_texto)
    palavras_unicas = dict(zip(lista_texto, palavras))
    
    plt.bar(palavras_unicas.keys(), palavras_unicas.values())
    plt.title("Contador de Palavras")
    plt.xlabel("Palavras")
    plt.ylabel("Frequência")
    plt.show()

win = Tk()
win.title("Contador de Palavras")

label = Label(win, text="Digite ou cole o texto:")
texto = Text(win, height=10, width=50)
botao = Button(win, text="Contar Palavras", command=contar_palavras)
novo_resultado = Label(win, text="Resultado:")

label.pack()
texto.pack()
botao.pack()
novo_resultado.pack()
win.geometry("400x300")
win.mainloop()
🚀 Como rodar
Certifique-se de ter o Python instalado.

Instale a biblioteca matplotlib se ainda não tiver:

bash
Copiar
Editar
pip install matplotlib
Salve o código em um arquivo .py, por exemplo contador.py.

Execute com:

bash
Copiar
Editar
python contador.py
🛠️ Requisitos
Python 3.x

tkinter (já vem com o Python na maioria das distros)

matplotlib
