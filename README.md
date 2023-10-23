import tkinter as tk
JanelaTabuleiro = tk.Tk()
JanelaTabuleiro.title("Tabuleiro")
n = 8
def CorQuadrado(linha, coluna):
    if (linha + coluna) % 2 == 0:
        return "white"
    else:
        return "black"
def ClicarQuadrado(clique):
    coluna = clique.widget.coluna
    linha = clique.widget.linha
    print(f"Clique no quadrado ({linha}, {coluna})")
for linha in range(n):
    for coluna in range(n):
        color = CorQuadrado(linha, coluna)
        square = tk.Frame(JanelaTabuleiro, width=70, height=70, background=color)
        square.grid(row=linha, column=coluna)
        square.linha = linha
        square.coluna = coluna
        square.bind("<Button-1>", ClicarQuadrado)

JanelaTabuleiro.mainloop()
