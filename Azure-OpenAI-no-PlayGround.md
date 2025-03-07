# Aula do Azure OpenAI no PlayGround

No bootcamp criei minha conta no Azure para ter acesso a ferramenta.

Entendi que o Playground, é uma área do Azure OpenIA para treinar modelos e criar prompts

Sobre a tokenização, entendi que é uma ação de dividir o texto em partes que podem ser palavras, subpalavras (junção de 2 palavras que formam 1 palavra) ou caracteres. Esta ação é importante para o Processamnto de Linguagem Natural(PNL), pois ajuda o entendimento da linguagem humana pelas máquinas, onde facilita a identificação de padrões pelos algoritmos.

O System Message modela o contexto inicial do modelo. É preciso definir o escopo do que será trabalhado, do contrário o modelo será muito generalizado fazendo com que as respostas sejam amplas demais, mostrando um ineficiente resultado esperado. Então o ideal é ser específico quanto ao assunto a ser tratado (por exemplo: vamos falar de notebooks, somente), definir todos os limites, estabelecer os pré requisitos, o "tom da resposta" - se será técnico ou de amplo entendimento. Compreensão sobre o assunto é essencial para abastecer o modelo (LLM) com exemplos de respostas esperadas para que ele compreenda o que deve ser feito. Uma forma de treinar o modelo é com o uso de "Shots" que nada mais são do que maneiras de como a LLM tem que ser portar. Ou seja, serão imputados exemplos de perguntas de usuários e as respostas esperadas para estas perguntas.
E dessa forma começamos a aprofundar em como conduzir o modelo para que ele seja o mais fidedigno possível, ressalvando que nenhuma resposta será totalmente fidedigna.
Aqui entram os conceitos de zero-shot, temperatura e top-p.
Em zero-shot podemos trabalhar sem exempls, com respostas diretas e respostas baseada apenas no prompt.
A temperatura (escolhe o que usar) pode ser criada em níveis, onde o "0" teremos respostas muito previsíveis (deterministicas) - recomendado para assuntos técnicos, códigos de programação. Já no nível "1" entregará respostas muito abrangentes, que podem acabar sendo interpretadas como improváveis  ou sem sentido, mas que é útil quando de deseja realizar brainstorm, criação de conteúdos, ter criatividade seja em escrita ou imagem. Diante disto a dúvida acaba sendo qual temperatura usar, então? Um começo é usar o padrão (0.7), fazer interação e documentar. Conforme se obtém as respostas, então realiza o ajuste da temperatura.
O top-p (determina o que pode ser usado) está relacionada a quais palavras podem ser usadas para entregar a resposta da interação, irá selecionar o que passar para a frente. Quanto maior o top-p, maior será a quantidade de palavras selecionadas

