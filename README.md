# Projeto_Final_Python
Projeto simples em python, feito para nota da disciplina Programação I
from builtins import range

print(95*"=")
print(30*"=",'\033[7;30m CAMPEONATO BAIANO DE FUTEBOL 2018 \033[m',30*"=")
print(95*"=")

num = int(input('\033[7;30m Digite a quantidade de times: \033[m'))
times = list(range(num))
print(35*"-")

pontosTime = 0
qndgolsprimeiro = list(range(num))
qndgolssegundo = list(range(num))
jogTime1Gols = list(range(num))
jogTime2Gols = list(range(num))

def entrada():
    for a in range(num):
        times[a] = input('\033[7;30m Informe o nome dos times: \033[m')
entrada()

print('')
def mostraTimes():
    for i in range(num):
        print('\033[7;30m indice [ {} ] nome do time [ {} ] \033[m'.format(i,times[i]))
mostraTimes()
print(35*"-")

print('')
def confrontos():
    for i in range(num-1):
        for j in range(i+1,num):
            print("\033[7;30m confrontos -- [{}] VS [{}] \033[m".format(times[i],times[j]))
confrontos()
print(35*"-")

print('')
def vencedor():
    cont=1
    for i in range(num-1):
        for j in range(i+1,num):
            #venc = int(input('Vencedor do {} confronto ?? -- Digite [{}] se for [{}] ou digite [{}] se for [{}]'.format(cont,i,times[i],j,times[j])))
            #cont = cont + 1
            print('\033[7;30m Placar do {} confronto --  [{}] VS [{}] \033[m'.format(cont, times[i],times[j]))
            qndgolsprimeiro = int(input('Número de gols de {} '.format(times[i])))
            qndgolssegundo = int(input('Número de gols de {} '.format(times[j])))
            #gols[i] = gols[i] + qndgolsprimeiro

            if (qndgolsprimeiro > qndgolssegundo):
                venc = i
                print(35 * "=")
                print('Vencedor {} '.format(times[i]))
                print(35 * "=")
                print('\033[7;30m Quem fez os gols da partida? - Nº camisa de [1] - [11] : \033[m')
                for a in range(qndgolsprimeiro):
                    jogTime1Gols = int(input('Quem fez {} gol do time [{}] '.format(a+1, times[i])))
                print(35 * "-")
            elif (qndgolsprimeiro < qndgolssegundo):
                venc = j
                print(35 * "=")
                print('Vencedor {} '.format(times[j]))
                print(35 * "=")
                print('\033[7;30m Quem fez os gols da partida? - Nº camisa de [1] - [11] : \033[m')
                for b in range(qndgolssegundo):
                    jogTime2Gols = int(input('Quem fez {} gol do time [{}] '.format(b+1, times[j])))
                print(35 * "-")
            else:
                print(35 * "=")
                print('Empate!!! 1 ponto para cada')
                print(35 * "=")
                print('\033[7;30m Quem fez os gols da partida? - Nº camisa de [1] - [11] : \033[m')
                jogTime1Gols = int(input('Quem fez gol do time {} '.format(times[i])))
                jogTime2Gols = int(input('Quem fez gol do time {} '.format(times[j])))
        #print(jogTime1Gols[i])
        #print(jogTime2Gols[j])
vencedor()

for i in range(num):    #PARTE INACABADA ...
    cont = 0
    #print(times[i])

    cont = cont + 3
    print('[{}] Pontos {}'.format(times[i], cont))
    print()

def pontos():
    for i in range(num - 1):
        cont = 0
        cont = cont + 3
        for j in range(i + 1, num): # CORRIGIR ESTE TRECHO...

        # print(times[i])
            if (qndgolsprimeiro > qndgolssegundo):
                #cont = cont + 3
                print('[{}] Pontos {}'.format(times[i], cont))
            elif (qndgolsprimeiro < qndgolssegundo):
                #cont = cont + 3
                print('[{}] Pontos {}'.format(times[j], cont))
            else:
                cont = cont + 1
                print('[{}] Pontos {}'.format(times[i], cont))
                print('[{}] Pontos {}'.format(times[j], cont))
pontos()
