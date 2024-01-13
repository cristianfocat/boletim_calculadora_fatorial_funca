def bolentim():
    n1=float(input('Primeira nota: '))
    n2 = float(input('Segunda nota: '))
    n3 = float(input('Terceira nota: '))
    n4 = float(input('Quarta nota: '))
    res=(n1+n2+n3+n4)/4
    print(res)
    cont=input("dejesa continuar? S/N: ").strip().lower()
    match cont:
        case 's':
            bolentim()
        case _:
            menu()

def calculadora():
    print('1-som\n2-sub\n3-div\n4-mul\n5-pot')
    escolha=input('Escolha a operação: ')
    n1=int(input("Primeiro numero: "))
    n2=int(input("segundo numero: "))
    match escolha:
        case '1':
            print(n1+n2)
        case '2':
            print(n1-n2)
        case '3':
            print(n1/n2)
        case '4':
            print(n1*n2)
        case '5':
            print(n1**n2)
        case _:
            print('operacao inexistente!!!')
    cont=input("dejesa continuar? S/N: ").strip().lower()
    match cont:
        case 's':
            calculadora()
        case _:
            menu()
def fatorial():
    s = 1
    n = int(input('Digite um número: '))
    for x in range(1, n + 1):
        s *= x
    print(f"O fatorial de '{n}' é: {s}")
    cont=input("dejesa continuar? S/N: ").strip().lower()
    match cont:
        case 's':
            fatorial()
        case _:
            menu()

def menu():
    print("\033[0m1-\033[34mBoletim\n\033[0m2-\033[32mcalculadora\n\033[0m3-\033[33mfatorial\n\033[0m4-\033[31mSair")
    escolha=input("\033[35mescolha o que vc quer: ")
    match escolha:
        case '1':
            bolentim()
        case '2':
            calculadora()
        case '3':
            fatorial()
        case '4':
            print('\033[30:44m========Até Mais😃==========')
            exit()
        case _:
            print('inexistente')
            menu()


menu()
