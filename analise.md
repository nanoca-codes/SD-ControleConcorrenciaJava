# Analise da atividade SD-ControleConcorrenciaJava

## Familia
Nas 3 execuções desse programa, foram mostradas problemas de concorrência, já que várias threads eestavam acessando a mesma conta sem nenhum tipo de sincronização. Os erros vistos por conta disso foram: leituras e escritas ao mesmo tempo, cada cliente tentando sacar o saldo integral, resultados diferentes em cada uma das execuções e saldos inconsistentes.


## Lock

Nas 3 execuções desse programa pode ser ser visto que a concorrência estava funcionando corretamente e de forma consistente, sem interferencia alguma ou falta de sincronização. Isso foi possivel pois o programa estava sincronizado, o que manteve a integridade do programa mesmo que vária threads estivessem concorrendo.
Pude observar com isso que: apenas duas threas conseguiram sacar um valor, fazendo com que a restante recebesse a mensagem de saldo insuficiente, não houve duplicação de saldo muito menos saques simultaneos incorretos, o saldo sempre seguia sequencia correta, a ordem das threads podia mudar mas o resultado final era sempre consistente. 


## RwLock

Nas 3 execuções todos os clientes tentaram sacar o valor integral ao mesmo tempo mas somente um conseguiu, enquanto para os outros uma mensagem de "saldo insuficiente foi mostrada. Isso aconteceu porque a sincronização de eventos está funcionando, evitando as condições de corrida e garantindo que apenas um cliente saque o valor que está disponivel, mantendo o saldo consistente e impendindo acessos incorretos.