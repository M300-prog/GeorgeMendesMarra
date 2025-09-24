Responder o questionário abaixo em seu GitHub (individual). Coloque as perguntas e respostas.

Exercícios Teóricos – Processos

1. Qual a diferença entre programa e processo?
-Programa é um conjunto estático de instruções,enquanto um processo é uma instância ativa e dinâmica de um programa em execução.
2. Quais são os estados de um processo e quando ocorrem as transições?
-Novo, Pronto, Em Execução, Bloqueado e Finalizado.
3. O que contém um Process Control Block (PCB)?
-Contém todas as informações que o sistema operacional precisa para gerenciar e executar um processo.
4. O que acontece com os recursos de um processo quando ele termina?
-Não há mais possibilidade de alteração da decisão, o processo retorna à sua origem para a execução da sentença.
5. Qual a diferença entre fork() e exec() no UNIX?
-No UNIX, fork() cria uma duplicata exata do processo atual, resultando em dois processos (pai e filho) a executar o mesmo código, enquanto exec() substitui o código e os dados do processo existente por um novo programa a ser executado.
6. Como funciona a hierarquia de processos em UNIX?
-Criação de processos "filhos" por um processo "pai", onde um processo filho recebe um identificador único e herda informações do seu pai, estabelecendo uma relação de árvore.
7. Compare memória compartilhada e troca de mensagens (IPC).
=Diferem na forma como os dados são partilhados. A memória compartilhada permite que processos acedam a uma região comum de memória, sendo o método mais rápido para transferir grandes quantidades de dados, mas exige mecanismos de sincronização para evitar condições de corrida.
8. Cite exemplos de chamadas de sistema usadas em IPC.
-pipe() e pipe2()
9. Por que é importante que o sistema operacional faça gerenciamento de processos?
-Permite a execução eficiente e simultânea de múltiplos programas (processos), garantindo que os recursos do sistema (como CPU e memória) sejam usados de forma otimizada, alocando-os e protegendo-os de maneira adequada.
10. Explique a diferença entre processos independentes e processos cooperativos.
-Processos independentes não interagem nem compartilham dados com outros processos e não podem ser afetados por eles, enquanto processos cooperativos podem afetar ou ser afetados por outros processos, necessitando de mecanismos de comunicação para trocar dados e informações.
11. O que é um processo zumbi em UNIX/Linux?
-È um processo que já terminou a sua execução, mas permanece na tabela de processos do sistema, ocupando um slot de ID de processo.
12. Explique a diferença entre chamadas bloqueantes e não bloqueantes em IPC.
-Chamadas bloqueantes fazem com que o programa que as executa espere até que a operação de comunicação seja concluída antes de prosseguir, enquanto chamadas não bloqueantes retornam imediatamente, permitindo que o programa continue executando outras tarefas enquanto a comunicação está em andamento.
13. Qual a diferença entre processo pesado (process) e thread (processo leve)?
-um processo (pesado) possui seu próprio espaço de memória isolado, enquanto threads (leves) compartilham o mesmo espaço de memória dentro de um processo.
14. Por que sistemas operacionais multiprogramados precisam de troca de contexto (context switch)?
-É o processo em que o sistema operacional salva o estado de um processo (valores dos registradores, contador de programa, pilha, etc.) e carrega o estado de outro processo para que ele possa continuar a execução de onde parou.
15. Cite vantagens e desvantagens da comunicação via memória compartilhada.
-Vantagens:
Rapidez – como os processos acessam diretamente a memória, a comunicação é mais rápida do que em outros métodos (ex.: troca de mensagens).

Grande volume de dados – permite transferir grandes quantidades de informação de forma eficiente.

Baixa sobrecarga – não precisa de chamadas frequentes ao sistema operacional depois da configuração inicial. 
-Desvantagens:

Sincronização necessária – os processos podem sobrescrever dados uns dos outros se não houver controle (precisa de semáforos, mutex, etc.).

Complexidade maior – o programador deve implementar mecanismos de coordenação.

Problemas de segurança/isolamento – processos diferentes têm acesso ao mesmo espaço de memória, o que pode gerar erros ou vulnerabilidades.
