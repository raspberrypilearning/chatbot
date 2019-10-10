## Um robô falante

Agora que tens um robô falante com personalidade, vamos programá-lo para conversar contigo.

\--- task \---

Clica no teu actor do robô e adiciona-lhe este código para que ` quando ele for clicado ` {: class = "block3events"}, ` pergunte o teu nome ` {: class = "block3sensing"} e, em seguida, ` diga "Que nome tāo bonito!" ` {: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
quando alguém clicar em ti
pergunta [Como te chamas?] e espera pela resposta
diz [Que nome tāo bonito!] durante (2) s
```

\--- /task \---

\--- task \---

Clica no teu robô para testar o teu código. Quando o robô perguntar o teu nome, digita-o na caixa que aparece na parte inferior do Palco e clica na marca azul, ou pressiona <kbd>Enter</kbd>.

![Testing a ChatBot response](images/chatbot-ask-test1.png)

![Testing a ChatBot response](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

De momento, o teu robô responde "Que nome tāo bonito!" todas as vezes que respondes. Podes tornar a resposta do robô mais pessoal, para que a resposta seja diferente sempre que um nome diferente for digitado.

Altera o código do actor robô para ` juntar ` {: class = "block3operators"} "Olá" com a `resposta` {: class = "block3sensing"} para a pergunta "Como te chamas?", de maneira a que fique assim:

![nano sprite](images/nano-sprite.png)

```blocks3
quando alguém clicar em ti
pergunta [Como te chamas?] e espera pela resposta
diz (a junção de [Olá] com (a resposta) :: +) durante (2) s
```

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Ao armazenar a resposta numa **variável**, podes usá-la em qualquer lugar do teu projeto.

Cria uma nova variável chamada `nome`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Agora, altera o código dos actores do teu robô para definir a variável ` nome ` {: class = "block3variables"} como ` resposta ` {: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
quando alguém clicar em ti
pergunta [Como te chamas?] e espera pela resposta

+ altera [nome v] para (a resposta)
diz (a junção de [Olá ] com (nome :: + variables)) durante (2) s
```

O teu código deve funcionar como antes: o teu robô falante deve dizer olá usando o teu nome.

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

Test your program again. Notice that the answer you type in is stored in the `name`{:class="block3variables"} variable, and is also shown in the top left-hand corner of the Stage. To make it disappear from the Stage, go to the `Data`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.