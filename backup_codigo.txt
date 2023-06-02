# Importo a biblioteca OS para poder usar no final para apagar a tela caso a pessoa queira gerar mais de uma tabuada.
import os

print("Bem vindo ao gerador de tabuada")
print("Orientação:Somente informar números positivos acima de zero")


# Crio todo o código em função para poder criar um loop se a pessoa querer gerar mais de uma tabuada.
def gerador():
    # Garanto que a tabuada e numero máximo começa em -1.
    tabuada = -1
    numero_maximo = -1

    # Crio um loop para garantir que a tabuada e numero máximo não seja negativo
    # Peço para a pessoa qual tabuada ela quer gerar. Exemplo: tabuada de 2
    while tabuada <= -1:
        tabuada = int(input("Primeiro digite qual tabuada você quer gerar "))

    # Peço para a pessoa qual o multiplicador máximo. Exemplo: tabuada de multiplicador 10
    while numero_maximo <= -1:
        numero_maximo = int(input("Agora digite qual o multiplicador maximo da sua tabuada "))

    print("Tabuada de " + str(tabuada))

    # Crio a função do cálculo do gerador de tabuada
    def funcao():
        # Garanto que meu multiplicador inicia em zero.
        # Crio meu loop que fica rodando até que o número multiplicador seja igual ao número máximo .
        # A cada rodada, ele printa a tabuada com o resultado
        multiplicador = 0
        while multiplicador != numero_maximo + 1:
            resultado = tabuada * multiplicador
            print(str(tabuada) + "X" + str(multiplicador) + "=" + str(resultado))
            multiplicador = multiplicador + 1

    print("-----------")
    funcao()
    print("-----------")

    # Após gerado a tabuada, pergunto se a pessoa quer gerar outra tabuada, se sim vai para começo do programa.
    # Caso ela não deseja gerar outra tabuada, finaliza o programa.
    print("Voce deseja gerar outra tabuada?")
    sair = input("sim ou nao = ")
    if sair == "sim":
        os.system('cls')
        gerador()
    else:
        print("Obrigado por usar o gerador de tabuada")
        print("Criado por Elyel B. Pedroso")
        print("Pressione Enter para sair")
        input()


gerador()
