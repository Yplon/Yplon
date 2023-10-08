from tkinter import *
import sys
import os

'''def teste1():
    # Criando texto de orientação
    escolha_modo1 = Label(janela_jogo, text="ESCOLHAODO DE JOGO", bg="black", foreground="white", font=("Arial", 10))
    # bg=para mudar cor background /// foreground=para mudar cor da letra
    escolha_modo1.grid(column=0, row=0, pady=100, padx=200)

    # Criando Botão para 1v1
    botao_1v11 = Button(janela_jogo, text="PvP", font=("Arial", 10), command=teste1)
    botao_1v11.grid(column=0, row=1, pady=50, padx=10)

    # Criando Botão para Jogador x PC
    botao_jxpc1 = Button(janela_jogo, text="Jogador xC", font=("Arial", 10), bg="black")
    botao_jxpc1.grid(column=0, row=2, pady=10)
'''
def jogar_1v1():
    janela_jogo.withdraw()
    import teste




janela_jogo = Tk()
janela_jogo.title("Dama")
janela_jogo.geometry("800x600")
janela_jogo.config(bg="black")

#Criando texto de orientação
escolha_modo = Label(janela_jogo, text="ESCOLHA O MODO DE JOGO", bg="black", fg="white", font=("Poetsen One",20), )
#bg=para mudar cor background /// foreground=para mudar cor da letra
escolha_modo.grid(column=0, row=0, pady=100, padx=200)



#Criando Botão para 1v1
botao_1v1 = Button(janela_jogo, text="PvP", font=("Arial",20), bd=0, highlightthickness=0, command=jogar_1v1)
botao_1v1.grid(column=0, row=1, pady=50, padx=10, ipadx=60)

#Criando Botão para Jogador x PC
botao_jxpc = Button(janela_jogo, text="Jogador x PC", font=("Arial",20),bd=0, highlightthickness=0)
botao_jxpc.grid(column=0, row=2, pady=10)




janela_jogo.mainloop()

