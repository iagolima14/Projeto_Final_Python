# Projeto_Final_Python
Projeto simples em python, feito para nota da disciplina Programação I

#Projeto Final
vitorias = []
gols = []
print(45*"=")
print(5*"=",'CAMPEONATO BAIANO DE FUTEBOL 2018',5*"=")
print(45*"=")

num = int(input('Digite a quantidade de times:'))
times = list(range(num))
print(35*"-")

def entrada():
    for a in range(num):
        times[a] = input('Informe o nome dos times: ')
entrada()

print('')
def mostraTimes():
    for i in range(num):
        print('indice [ {} ] nome do time [ {} ]'.format(i,times[i]))
mostraTimes()
print(35*"-")

print('')
def confrontos():
    for i in range(num-1):
        for j in range(i+1,num):
            print("confrontos -- [{}] VS [{}]".format(times[i],times[j]))
confrontos()
print(35*"-")

print('')
def vencedor():
    cont=1
    for i in range(num-1):
        for j in range(i+1,num):
            venc = int(input('Vencedor do {} confronto ?? -- Digite [{}] se for [{}] ou digite [{}] se for [{}]'.format(cont,i,times[i],j,times[j])))
            cont = cont + 1
            qndgolsprimeiro = int(input('Número de gols de {} '.format(times[i])))
            qndgolssegundo = int(input('Número de gols de {} '.format(times[j])))
            #vitorias[venc] = vitorias[venc] + 3
            #gols[i] = gols[i] + qndgolsprimeiro
            #gols[j] = gols[j] + qndgolssegundo
vencedor()
print(35*"-")

for i in range(num):
    print(times[i])
    print()
    print()
