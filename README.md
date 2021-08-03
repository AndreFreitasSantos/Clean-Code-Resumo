
  

# Clean Code Resumo

É importante frisar que os conhecimentos e padrões aqui apresentados não apenas devem ser lidos, mas também é uma parte fundamental para o seu crescimento como programador colocar em prática, entendendo que haverão erros, e que isso é normal.

  

## O Custo De Ter Um Código Confuso

  
É importante perceber o fato de que quando as pessoas alteram um código ruim, elas tendem a piorá-lo ainda mais.

Uma equipe que começa a construção do projeto trabalhando rapidamente, com o tempo sentira o peso de um código mal escrito, onde cada nova alteração gera erros em outros lugares do mesmo código, o que força os desenvolvedores a remendar o código até que seja possível acoplar a alteração, o que faz o código cada vez mais ilegível, como um grande emaranhado de gambiarras sobre gambiarras.

Com a diminuição da produção da equipe, a empresa contrata novos desenvolvedores para aumentar a produtividade, mas como o código está mal escrito, gera confusão entre os novos membros, fazendo com que atrapalhem ainda mais na construção da aplicação, trazendo a produtividade da equipe ainda mais próxima de zero. Então é sempre importante deixar o código o mais limpo possível 

## Regras para ter um código bem escrito

### Nomes Significativos 

Variaveis, funções, parâmetros, classes, pacotes, arquivos-fonte e os diretórios que os possui. Todas essas e algumas outras coisas possuem nomes dados por nós. Nomeamos, nomeamos e nomeamos, como é algo que fazemos com bastante frequência, é melhor quue façamos isso bem não é? Vejamos a seguir regras para a criação de bons nomes.  

#### Nomes que revelem o seu propósito

Nomes que deixem claro sua função pode parecer algo óbvio, mas é muito importante gastar um certo tempo para ter certeza de que aquele é o nome correto, até porque, um nome mal elaborado pode te fazer perder bem mais tempo.

O nome de uma variável, função ou classe deve responder as princípais questões, deve dizer porque existe, o que faz e como é usado. Se um nome requer um comentário, então ele não revela o seu propósito.

```py
    int d; //Tempo decorrido em dias
```