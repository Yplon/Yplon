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
        Cor = CorQuadrado(linha, coluna)
        Quadrado = tk.Frame(JanelaTabuleiro, width=70, height=70, background=Cor)
        Quadrado.grid(row=linha, column=coluna)
        Quadrado.linha = linha
        Quadrado.coluna = coluna
        Quadrado.bind("<Button-1>", ClicarQuadrado)

JanelaTabuleiro.mainloop()
