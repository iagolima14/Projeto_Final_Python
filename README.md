# Projeto_Final_Python
Projeto simples em python, feito para nota da disciplina Programação I

#Projeto Final
pontos = ()
gols = ()
print(95*"=")
print(30*"=",'CAMPEONATO BAIANO DE FUTEBOL 2018',30*"=")
print(95*"=")

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
            #venc = int(input('Vencedor do {} confronto ?? -- Digite [{}] se for [{}] ou digite [{}] se for [{}]'.format(cont,i,times[i],j,times[j])))
            #cont = cont + 1
            print('Placar do {} confronto --  [{}] VS [{}]'.format(cont, times[i],times[j]))
            qndgolsprimeiro = int(input('Número de gols de {} '.format(times[i])))
            qndgolssegundo = int(input('Número de gols de {} '.format(times[j])))
            #gols[i] = gols[i] + qndgolsprimeiro

            if (qndgolsprimeiro > qndgolssegundo):
                venc = i
                print(35 * "=")
                print('Vencedor {} '.format(times[i]))
                #pontos[i] += 3
                print(35 * "=")
                print('Quem fez os gols da partida? - Nº camisa de [1] - [11] :')
                for a in range(qndgolsprimeiro):
                    jogTime1Gols = int(input('Quem fez {} gol do time {} '.format(a+1, times[i])))
                print(35 * "-")
            elif (qndgolsprimeiro < qndgolssegundo):
                venc = j
                print(35 * "=")
                print('Vencedor {} '.format(times[j]))
                print(35 * "=")
                print('Quem fez os gols da partida? - Nº camisa de [1] - [11] :')
                for b in range(qndgolssegundo):
                    jogTime2Gols = int(input('Quem fez {} gol do time {} '.format(b+1, times[j])))
                print(35 * "-")
            else:
                print(35 * "=")
                print('Empate!!! 1 ponto para cada')
                print(35 * "=")
                print('Quem fez os gols da partida? - Nº camisa de [1] - [11] :')
                jogTime1Gols = int(input('Quem fez gol do time {} '.format(times[i])))
                jogTime2Gols = int(input('Quem fez gol do time {} '.format(times[j])))
vencedor()

for i in range(num):    #PARTE INACABADA ...
    print(times[i])
    print()
    print()
