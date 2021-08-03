
  

  

### Clean Code Resumo

  

É importante frisar que os conhecimentos e padrões aqui apresentados não apenas devem ser lidos, mas também é uma parte fundamental para o seu crescimento como programador colocar em prática, entendendo que haverão erros, e que isso é normal.

  

  

# O Custo De Ter Um Código Confuso

  

É importante perceber o fato de que quando as pessoas alteram um código ruim, elas tendem a piorá-lo ainda mais.

  

Uma equipe que começa a construção do projeto trabalhando rapidamente, com o tempo sentira o peso de um código mal escrito, onde cada nova alteração gera erros em outros lugares do mesmo código, o que força os desenvolvedores a remendar o código até que seja possível acoplar a alteração, o que faz o código cada vez mais ilegível, como um grande emaranhado de gambiarras sobre gambiarras.

  

Com a diminuição da produção da equipe, a empresa contrata novos desenvolvedores para aumentar a produtividade, mas como o código está mal escrito, gera confusão entre os novos membros, fazendo com que atrapalhem ainda mais na construção da aplicação, trazendo a produtividade da equipe ainda mais próxima de zero. Então é sempre importante deixar o código o mais limpo possível

  

## Regras para ter um código bem escrito

  

### Nomes Significativos



Variaveis, funções, parâmetros, classes, pacotes, arquivos-fonte e os diretórios que os possui. Todas essas e algumas outras coisas possuem nomes dados por nós. Nomeamos, nomeamos e nomeamos, como é algo que fazemos com bastante frequência, é melhor quue façamos isso bem não é? Vejamos a seguir regras para a criação de bons nomes.

  

### Nomes que revelem o seu propósito

  

Nomes que deixem claro sua função pode parecer algo óbvio, mas é muito importante gastar um certo tempo para ter certeza de que aquele é o nome correto, até porque, um nome mal elaborado pode te fazer perder bem mais tempo.

  

O nome de uma variável, função ou classe deve responder as princípais questões, deve dizer porque existe, o que faz e como é usado. Se um nome requer um comentário, então ele não revela o seu propósito.

  

~~~java

int d; //Tempo decorrido em dias

~~~


O nome "```d```" não revela absolutamente nada sobre sua função no código, deveríamos escolher um nome para especificar seu uso e a unidade usada, como por exemplo:

~~~java

int tempoDecorridoEmDias;
int diasDesdeCriacao;
int diasDesdeModificacao;
int idadeArquivoEmDias;

~~~

Escolher bons nomes facilita bastante o entendimento e a manutenção do código não é? Agora tente entender o que faz esse código: 


~~~java

public List<int[]> getThem(){
	List<int[]> list1 = new Arraylist<list[]>();
	for(int[] x : Lista)
		if (x[0] == 4)
			 list1.add(x)
		return list1;
}

~~~

Por que é tão difícil dizer o que faz esse pequeno código? Não há expressões complexas.

O código tem uma boa endentação, temos apenas três variáveis e duas constantes. Nem mesmo temos classes ou métodos  polimórficos. Apenas uma lista de vetores (ao que parece). Ou seja, o problema não é a complexidade do código que estamos  lendo, e sim qual o contexto em que ele está inserido, o que está completamente oculto. Deveríamos ser capazes de apenas olhando responder:

1. Que tipo de coisas temos em Lista?
2. Qual a importância do índice zero em Lista?
3. Qual a importância do 4?
4. Como seria usada a lista retornada?


Agora sabendo que este código tem haver com um jogo de campo minado, que "theList" armazena os quadrados do jogo. Não seria muito melhor renomeá-la para "tabuleiro"?

### Evite informações erradas

Cada quadrado do tabuleiro é representado por um vetor simples, onde o índice zero armazena um valor de status e que o valor 4 significa "Marcado com uma bandeira". Ao renomear podemos agora ter um código muito mais inteligível:

~~~java

public List<int[]> PegarQuadradosComBandeira(){
	List<int[]> quadradosComBandeira = new Arraylist<list[]>();
	for(int[] x : tabuleiro)
		if (x[STATUS] == Bandeira)
			 quadradosComBandeira.add(x)
		return quadradosComBandeira;
}

~~~