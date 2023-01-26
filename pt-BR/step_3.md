## Um ChatBot falante

Agora que você tem um chatbot com uma personalidade, você vai programá-lo para falar com você.

\--- task \---

Clique no seu ator de chatbot e adicione este código a ele para que `quando ele for clicado`{:class="block3events"}, ele `peça o seu nome`{:class="block3sensing"} e então `diga"Que nome adorável!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

\--- /task \---

\--- task \---

Clique no seu chatbot para testar seu código. Quando o chatbot solicitar seu nome, digite-o na caixa que aparece na parte inferior do Palco e clique na marca azul ou pressione <kbd> Enter. </kbd>.

![Testando uma resposta do ChatBot](images/chatbot-ask-test1.png)

![Testando uma resposta do ChatBot](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Neste momento, o seu chatbot responde "Que nome adorável!" toda vez que você responder. Você pode tornar a resposta do chatbot mais pessoal, para que a resposta seja diferente toda vez que um nome diferente for digitado.

Mude o código do ator do chatbot para `juntar `{:class="block3operators"} "Oi" com a `resposta`{:class="block3sensing"} para "Qual é o seu nome?", para que o código fique assim:

![ator nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![Testando uma resposta personalizada](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Ao armazenar a resposta numa **variável**, você pode usá-la em qualquer lugar do seu projeto.

Cria uma nova variável chamada `nome`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Agora, mude o código do seu ator do chatbot para definir a variável `nome`{:class="block3variables"} como `resposta`{:class="block3sensing"}:

![ator nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

Seu código deve funcionar como antes: seu chatbot deve dizer oi usando o nome que você digitou.

![Testando uma resposta personalizada](images/chatbot-answer-test.png)

\--- /task \---

Teste seu programa novamente. Observe que a resposta que você digita é armazenada no `nome`{:class="block3variables"} e também é mostrada no canto superior esquerdo do Palco. Para fazê-lo desaparecer do palco, vá para a seção de blocos `Variáveis`{:class="block3variables"} e clique na caixa ao lado do `nome`{:class="block3variables"} para que ela não seja marcada.