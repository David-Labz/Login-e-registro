usuarios = {}

def registrar_usuario():

    nome_usuario = input("Digite o nome de usuário desejado: ")
    senha = input("Digite a senha desejada: ")
    usuarios[nome_usuario] = senha
    print("Usuário registrado com sucesso!")

def fazer_login():

    nome_usuario = input("Digite seu nome de usuário: ")
    senha = input("Digite sua senha: ")
    if nome_usuario in usuarios and usuarios[nome_usuario] == senha:
        print("Login bem-sucedido!")
    else:
        print("Nome de usuário ou senha incorretos.")

def menu():

    while True:
    
        print("\nBem-vindo ao sistema de login!")
        print("1. Registrar novo usuário")
        print("2. Fazer login")
        print("3. Sair")
        escolha = input("Escolha uma opção: ")

        if escolha == "1":
            registrar_usuario()
        elif escolha == "2":
            fazer_login()
        elif escolha == "3":
            print("Saindo do sistema.")
    
        else:
            print("Opção inválida. Por favor, escolha novamente.")

menu()
