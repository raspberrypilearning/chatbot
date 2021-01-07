## Um ChatBot falante

Agora que você tem um chatbot com uma personalidade, você vai programá-lo para falar com você.

\--- task \---

Click on your chatbot sprite, and add this code to it so that `when it's clicked`{:class="block3events"}, it `asks for your name`{:class="block3sensing"} and then `says "What a lovely name!"`{:class="block3looks"}.

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

Right now, your chatbot replies "What a lovely name!" every time you answer. You can make the chatbot’s reply more personal, so that the reply is different every time a different name is typed in.

Mude o código do ator do chatbot para `juntar `{:class="block3operators"} "Oi" com a `resposta`{:class="block3sensing"} para "Qual é o seu nome?", para que o código fique assim:

![nano sprite](images/nano-sprite.png)

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

Now, change your chatbot sprites’s code to set the `name`{:class="block3variables"} variable to `answer`{:class="block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

Seu código deve funcionar como antes: seu chatbot deve dizer oi usando o nome que você digitou.

![Testando uma resposta personalizada](images/chatbot-answer-test.png)

\--- /task \---

Teste seu programa novamente. Observe que a resposta que você digita é armazenada no `nome`{:class="block3variables"} e também é mostrada no canto superior esquerdo do Palco. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.