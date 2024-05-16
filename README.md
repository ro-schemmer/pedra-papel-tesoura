# pedra-papel-tesoura
jogo no phyton

import random  # Importa o módulo random para gerar escolhas aleatórias

def jogo_de_pedra_papel_tesoura(opcao_usuario):
    opcoes = ['🗿', '📄', '✂️']  # Define as opções possíveis do jogo como uma lista de emojis
    opcao_computador = random.choice(opcoes)  # O computador escolhe aleatoriamente uma das opções

    print("Você escolheu:", opcao_usuario)  # Exibe a escolha do usuário
    print("O computador escolheu:", opcao_computador)  # Exibe a escolha do computador
    
    # Lógica para determinar o resultado do jogo
    if opcao_usuario == opcao_computador:  # Se as escolhas forem iguais, é um empate
        return "Empate!"
    elif (opcao_usuario == '🗿' and opcao_computador == '✂️') or \
         (opcao_usuario == '📄' and opcao_computador == '🗿') or \
         (opcao_usuario == '✂️' and opcao_computador == '📄'):
        return "Você ganhou!"  # Se o usuário ganhar, retorna uma mensagem de vitória
    else:
        return "Você perdeu!"  # Se o usuário perder, retorna uma mensagem de derrota

# Exibe as opções para o usuário
print("Escolha sua jogada:")
print("1 - Pedra 🗿")
print("2 - Papel 📄")
print("3 - Tesoura ✂️")

# Solicita a escolha do usuário e verifica a entrada
opcao = input("Digite o número correspondente à sua escolha: ")

# Chama a função do jogo com base na escolha do usuário e exibe o resultado
if opcao == '1':
    resultado = jogo_de_pedra_papel_tesoura('🗿')
elif opcao == '2':
    resultado = jogo_de_pedra_papel_tesoura('📄')
elif opcao == '3':
    resultado = jogo_de_pedra_papel_tesoura('✂️')
else:
    resultado = "Escolha inválida!"  # Se a escolha for inválida, exibe uma mensagem de erro

print(resultado)  # Exibe o resultado do jogo
