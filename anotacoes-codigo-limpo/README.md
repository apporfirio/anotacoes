# O que é o Código Limpo?

Estilo de programação que visa desenvolver software de **fácil manutenção**.

# Característicos

Software que atende ao Código Limpo satisfaz as seguintes características:

- Fácil leitura e entendimento.
- Simples, direto ao ponto.
- Segue padrões.
- Coberto de testes.
- Eficiente.
- Elegante.

Um código limpo **"Parece ter sido escrito por alguém que se importa"** (Michael Feathers).

# Regras Práticas

## Nomes

- Devem ser descritivos e pronunciáveis.
- Devem revelar a intenção central por de sua existência.
- Métodos devem ser nomeados por verbos ou frases verbais.
- Classes e objetos devem ser nomeados por substantivos.
- Devem ser únicos para cada conceito, evitando-se sinônimos. Exemplo: escolher e manter um apenas dentre 'fetch', 'retrieve', 'find', 'get'
ao nomear métodos que buscam um objeto/valor em algum container.

## Métodos

- Devem fazer apenas uma coisa e fazê-la bem (Princípio da Responsabilidade Única).
- Devem ser pequenos, objetivos (< 20 linhas, < 150 caracteres por linha).
- Trechos de código auxiliares à função do método devem ser extraídos para métodos auxiliares.
- Um parâmetro booleano deve dar origem a dois métodos ambos sem esse parâmetro booleano, cada método sendo responsável por um caso.
- Não retorne null, retorne coleções vazias ao invés.

## Exceções

- Não retorne códigos de erros ou strings com mensagens de erros, lance exceções ao invés.

## Formatação

- Variáveis devem ser declaradas o mais próximo possível do seu uso.
- Métodos auxiliares devem estar próximos, e abaixo, do método invocador.s
- O estilo do projeto, e não o estilo pessoal, deve ser preservado.


## Comentários

- Ao invés de se dizer com comentários, diga com o código.
- São úteis para explicar características de negócio e licença de uso.


# Referências
- https://becode.com.br/clean-code/
- https://pt.slideshare.net/rodrigokono/boas-prticas-tcnica-para-um-cdigo-limpo-clean-code
- https://pt.slideshare.net/arturoherrero/clean-code-8036914