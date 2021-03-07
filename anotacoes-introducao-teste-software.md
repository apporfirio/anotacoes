# Verificação e Validação

Com a finalidade de nos certificarmos de que um software atenderá as necessidades de seus usuários,
podemos **verificá-lo** e **validá-lo**.

- **Verificação**
  
    - Processo de checagem da conformação do software à sua especificação (que é derivada dos requisitos de usuário);
    - Processo que responde à pergunta "Estamos desenvolvendo corretamente?";
    - É feita antes da validação;
    - Exemplos:
      - Testes unitários mapeando comportamento de classes aos requisitos de usuário; 
      - Testes regressivos após refatoração;

- **Validação**

    - Processo de checagem do comportamento do software em relação às necessidades e à satisfação do usuário;
    - Processo que responde à pergunta "Estamos desenvolvendo o produto correto?";
    - Exemplos:
      - Checagem de modelo e protótipo junto ao usuário;
      - Entrevista com usuário para checar se os requisitos coincidem com as expectativas do usuário para o comportamento do sistema;


# Técnicas de Verificação e Validação

As seguintes técnicas podem ser aplicadas durante o ciclo de desenvolvimento.

- Inspeção de código (Code Review);
- Discussão de design de modelo e código;
- Análise estática de código;
- Testes;
- Verificação em tempo de execução;


# Por que verificar e validar software?

- Porque desenvolver software é uma tarefa difícil e seres humanos cometem erros;
- Erros em software podem causar má propaganda, prejuízo financeiro e mortes;


# Por que testar software?

- A técnica de teste de software é a única atualmente existente para se **detectar defeitos**
quando um software encontra-se em seu ambiente de execução, o qual inclui não apenas o software desenvolvido
mas todos os demais softwares usados, desde o sistema operacional, e também o hardware subjacente;

- A técnica de teste de software também é utilizada para se observar alguns comportamentos, 
como, por exemplo, **performance de execução**;

- Testes também são utilizados como evidência de comportamento esperado para sua aceitação por parte de clientes;

- Testes também servem como uma ferramenta de documentação de comportamento esperado (TDD);


# Limitação da Técnica de Teste

Uma vez que o **número de possíveis casos de execução e comportamentos** a serem contemplados, mesmo para pequenos programas, é em geral
muito grande, então a técnica de teste de software é em geral **incompleta**.

Para que um software fosse testado por **completo**, teríamos que **contemplar** com os testes **todos os possíveis estados** do sistema.

Como o espaço de estados de um sistema é discreto e, portanto, não contínuo, não é possível realizar extrapolações para estados vizinhos
após um teste bem sucedido de um determinado estado, diferentemente do que acontece com sistemas físicos clássicos, que são contínuos.


# Como ser um bom testador

- Conhecer os requisitos daquilo sendo testado;
- Ter em mente onde é comum cometer-se erros, por exemplo, em input com valores de contorno e em expressões booleanas complexas;
- Mentalidade investigativa: 'O que este programa tem que fazer?', 'Como este programa pode quebrar?';


# Escala de Testes

- Unidade: testes de métodos ou classes;
- Integração: testes de módulos ou pacotes;
- Sistema: testes de todo o sistema; 


# Processos de Testes

- Antes (TDD): primeiro escrevem-se os testes e depois o código para passar nesses testes;

- Depois (Padrão): primeiro escreve-se o código e depois os testes para verificar se o código faz o esperado;


# Estratégias de Testes

- Black Box
    - É o tipo de teste que compara o comportamento observado com os requisitos sem ser influenciado pela implementação 
do comportamento que se quer testar;
 
- White Box
    - É o tipo de teste baseado no conhecimento que se tem da implementação do comportamento que se quer testar;


# Tipos de Testes

- Testes Funcionais;
- Testes de Usabilidade;
- Testes de Aceitação;
- Testes de Regressão;
- Testes de Segurança;
- Testes de Performance;
- Testes de Disponibilidade;


# Anatomia de um Teste Unitário

Um teste unitário é composto por:

- Unidade (método, função, classe) de software a ser testada;

- Caso de teste
  - Dados de entrada (input do teste);
  - Resultado/comportamento esperado;

- Oráculo (um humano ou um software que compara se o resultado/comportamento obtido para o input fornecido é igual ao resultado/comportamento esperado);


# Etapas de um Teste

A execução de um teste se dá em quatro etapas:

- Configuração
  - Definição, caso necessário, do estado/condição inicial em que a unidade de software a ser testada precisa estar para o caso de teste em
  questão;

- Invocação
    - Execução da unidade de software a ser testada com os dados de entrado do caso de teste;

- Avaliação
  - Comparação do resultado/comportamento obtido após a etapa de Invocação com o resultado/comportamento esperado do caso de teste;

- Limpeza
  - Remoção do estado/condição inicial definido na etapa de Configuração e de qualquer efeito causado durante a etapa de Invocação;


# Princípios de Teste

- **O que** queremos obter realizando testes? 
 - Desenvolver um processo rigoroso, eficiente e repetitível que permita a obtenção de qualidade para um software. 
   - A qualidade de um software é dividida em dois grupos:
     
     - Interna
       - Reusabilidade;
       - Modificabilidade;
       - Modularidade;
       - Extensabilidade;

     - Externa
       - Usabilidade;
       - Disponibilidade;
       - Confiabilidade;
       - Corretude;
       - Segurança;
       - Perfomance;
       - Portabilidade;
       - Interoperabilidade;


- **Onde** devemos focar os testes?
  - Nas áreas de código onde erros humanos são mais provavéis de ocorrer:
      - Módulos centrais para a performance de um sistema ou que possuem as regras de negócio mais complicadas;
        - 20% dos módulos de um sistema contém 80% dos bugs de um sistema antes de seu lançamento;
      
      - Valores de contorno em expressões;
     
      - Condições booleanas complexas;
      
      - Casting entre tipos (principalmente numéricos);
      
      - Condições de corrida e deadlocks;

- **Como** os testes devem ser realizados?
  - Para que o processo de teste seja rigoroso, é necessário que o mesmo seja feito por partes, em níveis crescentes de abstração, pois testar rigorosamente um sistema como um todo é muito difícil;
  
  - Aplicando diferentes técnicas de teste para atacar diferentes tipos de bugs;

  - Escrevendo testes uniformes, isto é, testes que ou sempre sucedem ou sempre falham. Testes que às vezes sucedem ou falham ('flakey tests')não são úteis;

- **Quando** devemos realizar os testes?
 - O mais cedo possível e o mais frequente possível;

- **Quem** deve realizar os testes?
  - As mesmas pessoas que desenvolverem o código e outras pessoas dentro da empresa;
 

À partir desses princípios de teste construímos técnicas de teste e à partir destas construímos metodologias de teste. Por fim,
construímos ferramentas de automação do processo de teste.


## O Modelo 'V' de Desenvolvimento de Software

É um modelo que divide as ações em duas categorias, Definição e Teste. 

Para cada ação em uma categoria existe uma ação correspondente na outra categoria.

Levantamento dos Requisitos de usuário (o que o usuário quer que o sistema faça) : Testes de aceitação (validacação)
Especificação (o que o sistema fará para atender aos requisitos de usuário)      : Testes de sistema   (verificação) 
Design e Arquitetura                                                             : Testes de integração de módulos
Implementação                                                                    : Testes de unidade               


Os **testes de unidade e de integração** são testes **white box**.

Os **testes de sistema** são testes **black box**. Estes testes **evidenciam** que a solução desenvolvida atende à sua **especificação**.

Os **testes de aceitação** são testes **black box** feitos à partir de dados de entrada provenientes do cliente. Estes estes **evidenciam** que a solução desenvolvida **atende aos requisitos de usuário**.


## Testes de Design e Verificação (DVT)

Contempla os testes de integração e os testes funcionais.

- Testes Funcionais
    - São realizados pelos testadores enquanto o desenvolvimento do sistema é feito.


## Testes de Validação de Sistema (SVT)

Contempla os testes de sistema e os testes não-funcionais.

- Testes Não-Funcionais
    São realizados pelos testadores para assegurar a qualidade (usabilidade, segurança, performance, etc) do comportamento entregue.


## Teste Estrutural 

É uma estratégia de teste **white box** que almeja realizar testes para que se cubra determinadas estruturas do código fonte (statements e expressões condicionais, por exemplo). Por 'cobrir' quer-se dizer que durante a execução dos testes, tais estruturas devem ser executadas.

A porcentagem de cobertura varia conforme o nível de exigência. Por exemplo, padrões de software para Aviação requerem 100% de cobertura
de statements.


## Teste de Mutação

É uma estratégia de calibração de um conjunto de testes atualmente existentes e bem sucedidos.

A estratégia consiste em se criar mutações no software que invalidam seu comportamento, cada mutação levando a uma nova versão do sistema. 

Uma mutação é uma falha cujo resultado possa ser observado. As mutações geralmente incluem: substituição de operadores e variáveis.

Os testes existentes são então executados contra cada versão mutante do sistema. 

Se os testes falharem, então os mesmos ganham credibilidade. Caso contrário, o conjunto existente de testes possui problemas de implementação.


## Plano de Teste

É o documento que descreve o escopo, o cronograma, os recursos e os critérios de entrada e saída
de qualquer atividade de teste.

O plano de teste é uma **ferramenta** que ajuda a:

- organizar o esforço de teste;
- escrever os casos de teste;
- comunicação entre desenvolvedores e negócio;


## Risco

Uma das finalidades do teste de software é a redução de risco de falha em sistemas lançados.

Por risco, quer-se dizer qualquer perca potencial associada a uma empresa:

- Financeira
- Reputação
- Licenças
- Funcionários
- Vidas

É quantificado por: impacto da falha x chance da falha ocorrer.

Quando há pouco tempo para testar, saber o risco de cada funcionalidade ajuda a decidir o que testar. 


## Relatório de Defeitos

Metade do tempo de um testador é destinado a escrever testes. 

A outra metade é destinada a atualizar testes já existentes e a escrever relatórios.

## Ciclo de Vida de Defeitos

- 1) Analisar o bug (encontrado durante testes automatizados ou reportado por alguém);
  - Encontrar a causa raíz: 
    - O teste está errado?
    - O testador está executando de modo inapropriado?
    - O software está errado?
  - Determinar se o erro é reproduzível ou repetitivo (ocorre mais de uma vez mas não de modo reproduzível). Analisar logs ajuda 
    a tornar um erro repetitivo em reproduzível.
  - Investigar a existência de outros caminhos que levem ao mesmo erro;

- 2) Reportar o bug;
  - Antes de ser escrito, deve-se verificar se já não existe um no sistema relato deste bug; 
  - Anatomia:
    - Identificação (ID, data)
    - Título do relatório
    - Descrição do problema
      - O que aconteceu (resultados observados).
      - O que deveria ter acontecido (resultados esperados).
      - O caso de teste usado.
      - Informações adicionais que podem ter influenciado os resultados observados.
    - Indicadores de estado
      - Estado geral (aberto ou fechado). 
      - Severidade.
      - Prioridade.
      - Estágio de resolução (Nenhum, Em processo, Corrigido).
    - Reprodução
      - Lista das configurações e passos a serem feitos afim de se reproduzir o problema.
    - Evidências
      - Qualquer tipo de mensagem de erro deve ser capturada e anexada como evidência.
      - Logs de erros.

- 3) Rastrear o status do conserto do bug, atualizando-o conforme mudar;
  
- 4) Nova análise do bug após o conserto ter sido feito;
    - Nesta etapa pode-se verificar se:
      - O problema foi corrigido;
      - O problema persiste;
      - Um novo problema surgiu;

- 5) Fechar o bug caso o mesmo tenha sido resolvido;


## Dublês de Testes

Para que se fossa realizar testes unitários em sistemas não triviais, é necessário que o sistema
se comunique com sistemas externos. Outro exemplo é quando vários desenvolvedores acessam uma mesma base de dados fazendo com que os testes unitários falhem ocasionalmente por conta da alteração da base. Além disso, em uma equipe de desenvolvimento distribuído,
um desenvolvedor precisará eventualmente testar sua tarefa sendo que esta possui dependência
de outra tarefa sendo feito concomitantemente por outro desenvolvedor.

Deste modo utilizamos dublês de testes para simular essas dependências.

Tipos de dublês de testes:

- Dummies
  - São valores usados apenas para atender a assinatura de métodos. Estes valores são irrelevantes para o teste do comportamento em questãod;

- Stubs
  - São respostas pré-prontas para invocações de métodos durante os testes;

- Fakes
  - Implementações leves de dependências pesadas. Por exemplo, um banco de dados em memória principal
    é usado como fake de um SGBD;

- Mocks
    - Permitem que se observe o comportamento de objetos Fakes;

- Spies
    - Permitem que se observe o comportamento de objetos não-Fakes, como, por exemplo, objetos de uma classe sendo testada.

Obs.: no framework Mockito, Stubs, Fakes e Mocks são todos chamados de 'mocks'.


## Serviço

Um **serviço** é um comportamento de sistema conforme percebido pelo usuário do sistema.


## Fracasso

Um **serviço** fracassa quando seu comportamento desvia da sua especificação.


## Erro

Um erro é a parte do sistema que leva a um fracasso. Pode ser latente (código equivado) ou efetivo (quando o código equivado é executado).


## Falha

Uma falha é a causa de um erro. Pode ser de origem humana ou de hardware. Assim, falha -> erro -> fracasso.


## Evasão de Falhas

Método para se prevenir falhas por meio de ações construtivas ou de design. Por exemplo: checagem, em tempo de compilação,
de operações inválidas; Diretrizes de implementação de software ('boas práticas');


## Tolerância a Falhas

Método para se lidar com falhas por meio de redundância de software ou de hardware. Por exemplo: múltiplos servidores para um mesmo website;


## Remoção de Erros

Método para se minimizar os erros latentes por meio de verificações. Por exemplo: com o uso da técnica de testes.


## Previsão de Erros

Método para se estimar a presença de erros e suas consequências e assim poder-se implementar medidas antecipadamente. 


## Confiabilidade

Medida da continuidade de tempo em que um serviço se comportamenta corretamente. 
Quantitativamente, é o tempo médio entre dois fracassos consecutivos (MTBF: mean-time between failures).


## Recuperabilidade

Medida de quão rápido um sistema tem seu funcionamento correto reparado após um fracasso.
Quantitativamente, é o tempo médio de reparo após um fracasso (MTTR: mean-time to repair).


## Disponibilidade

Medida da prontidão de um serviço para atender corretamente a requisições.
Quantitativamente, é igual a MTBF / (MTBF + MTTR).


