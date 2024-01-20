# IA-trabalho1

Este código representa uma solução para o problema do Mundo dos Blocos utilizando Inteligência Artificial. O Mundo dos Blocos é um problema clássico em IA que envolve mover blocos de uma configuração para outra, seguindo determinadas regras. O código fornecido está escrito em Prolog e utiliza um planejador de meios e fins com regressão de metas.

Arquivos:

    blocks_world.pl: Contém o código Prolog para a resolução do problema do Mundo dos Blocos.

Como Executar:

    Certifique-se de ter um interpretador Prolog instalado em sua máquina.
    Carregue o arquivo blocks_world.pl no seu interpretador Prolog.
    Defina seu estado inicial e metas usando os predicados state1/1 e final/1.
    Execute o predicado plan/3, passando o estado inicial, metas e uma variável para o plano como argumentos.

Predicados Prolog:

    can/2: Define as condições sob as quais uma ação específica pode ser realizada.

    adds/2 e deletes/2: Especifica os efeitos das ações no estado do mundo.

    object/1: Identifica objetos válidos no Mundo dos Blocos, que podem ser lugares ou blocos.

    impossible/2: Define condições que tornam impossível alcançar determinadas metas ou realizar certas ações.

    plan/3: O predicado principal para gerar um plano. Recebe o estado inicial, metas e uma variável para o plano, e busca recursivamente um plano para alcançar as metas especificadas.

    satisfied/2: Verifica se as metas são alcançadas no estado fornecido.

    select/3: Seleciona uma meta da lista de metas.

    achieves/2: Verifica se uma ação alcança uma meta específica.

    preserves/2: Verifica se uma ação preserva determinados relacionamentos no estado.

    regress/3: Calcula a regressão das metas após a realização de uma ação.

    addnew/3: Adiciona novas metas à lista de metas com base nas condições especificadas na ação.

    delete_all/3, member/2, delete/3: Predicados utilitários para manipulação de listas.

Detalhes Específicos do Mundo dos Blocos:

    O Mundo dos Blocos consiste em blocos (a, b, c, d) e lugares (1, 2, 3, 4, 5, 6).

    O tamanho de cada bloco é especificado usando o predicado size/2.

Exemplo:

prolog

?- state1(EstadoInicial), final(Metas), plan(EstadoInicial, Metas, Plano).

Isso gerará um plano para transformar o estado inicial no estado desejado.


Nota:

    Certifique-se de que o estado inicial e as metas estão definidos adequadamente com base no seu cenário específico do Mundo dos Blocos.

    Os predicados de exemplo state1/1 e final/1 demonstram como definir um estado inicial e metas finais.

    Você pode personalizar os blocos e lugares no Mundo dos Blocos, juntamente com seus tamanhos, para adequar à sua instância específica do problema.
