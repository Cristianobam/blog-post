# BERT - Bidirectional Encoder Representations from Transformers

Um dos grandes problemas na área de processamento de linguagem natural ([NLP][1]) é a escassez de dados de treino. Isso pode soar paradoxal uma vez que estamos submergidos em textos e mais textos na internet, contudo não é. A campo do NLP é diverso e com diversas aplicações. Até podemos achar alguns [datasets][2] com propósitos bem específicos, mas eles são pequenos, indo de alguns milhares até algumas centenas de milhares de dados com dados tags e labels. E como os os modelos de deep-learning modernos tanto para linguagem, quanto para outros propósitos se beneficiam das grandes quantidades de dados, temos alguns problemas.

[1]: bla.com
[2]: bla.com


Tendo isso em vista, os pesquisadores desenvolveram algumas técnicas para treinar modelos de linguagem bem generalistas. Imagine que estamos ensinando um cachorro a falar se frases são positivas ou negativas.

<div class="img-center">
<img src="https://media1.tenor.com/images/1940b67272ea2eeaf7c5b292f4ff8dc7/tenor.gif?itemid=6183942">
</div>

Podemos treinar o nosso canino nessa essa tarefa, mas será bem difícil e precisaremos de muitos exemplos de treino. Agora, vamos mudar a nossa estratégia. Ao invés de ensinar o nosso amigo a diferenciar frases positivas e negativas primeiro vamos ensiná-lo o que é a língua, o que são palavras, frases e como elas aparecem numa sentença. E não é que conseguimos?! Temos um cachorro versado em português agora. 

<div class="img-center">
<img src="https://media1.tenor.com/images/6b9a8f6e786326838f8f8a4a65a0ddd2/tenor.gif?itemid=4740643">
</div>

Agora que o nosso cão sabe o que são frases, como elas são compostas e as dependências dentro de uma sentença podemos ensiná-lo frases positivas e negativas. Como ele tem ess conhecimento bem amplo na língua não demora muito até ele aprender.

Na literatura isso é chamado de *pré-treino* e *ajuste fino* respectivamente. Dessa forma, pesquisadores usam corpus linguísticos extensos como a Wikepedia, ou o Google Books para fazer o pre-training dos modelos na língua e depois usam datasets menores ([IMDb][3], [YELP][4], [Tiny Shakespeare][5], [Amazon Reviews][6]) para fazer o fine-tunning.

[3]: [http://ai.stanford.edu/%7Eamaas/data/sentiment/]
[4]: [https://www.yelp.com/dataset]
[5]: [https://github.com/karpathy/char-rnn]
[6]: [https://s3.amazonaws.com/amazon-reviews-pds/readme.html]

To help close this gap in data, researchers have developed a variety of techniques for training general purpose language representation models using the enormous amount of unannotated text on the web (known as pre-training). The pre-trained model can then be fine-tuned on small-data NLP tasks like question answering and sentiment analysis, resulting in substantial accuracy improvements compared to training on these datasets from scratch. 