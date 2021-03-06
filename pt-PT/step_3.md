## Um robô falante

Agora que tens um robô falante com personalidade, vamos programá-lo para conversar contigo.

--- task ---

Clica no teu actor do robô e adiciona-lhe este código para que `quando ele for clicado`{:class="block3events"}, `pergunte o teu nome`{:class="block3sensing"} e, em seguida, `diga "Que nome tāo bonito!"`{:class="block3looks"}.

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Como te chamas?] and wait
say [Que nome tāo bonito!] for (2) seconds
```

--- /task ---

--- task ---

Clica no teu robô para testar o teu código. Quando o robô perguntar o teu nome, digita-o na caixa que aparece na parte inferior do Palco e clica na marca azul, ou pressiona <kbd>Enter</kbd>.

![Testar a resposta do robô falante](images/chatbot-ask-test1.png)

![Testar a resposta do robô falante](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

De momento, o teu robô responde "Que nome tāo bonito!" todas as vezes que respondes. Podes tornar a resposta do robô mais pessoal, para que a resposta seja diferente sempre que um nome diferente for digitado.

Altera o código do actor robô para `juntar`{:class="block3operators"} "Olá" com a `resposta`{:class="block3sensing"} para a pergunta "Como te chamas?", de maneira a que fique assim:

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Como te chamas?] and wait
say (join [Olá ] (answer) :: +) for (2) seconds
```

![Testar uma resposta personalizada](images/chatbot-answer-test.png)

--- /task ---

--- task ---

Ao armazenar a resposta numa **variável**, podes usá-la em qualquer lugar do teu projeto.

Cria uma nova variável chamada `nome`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Agora, altera o código dos actores do teu robô para definir a variável `nome`{:class="block3variables"} como `resposta`{:class="block3sensing"}:

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Como te chamas?] and wait
+ set [nome v] to (answer)
say (join [Olá ] (nome :: variables +)) for (2) seconds
```

O teu código deve funcionar como antes: o teu robô falante deve dizer olá usando o teu nome.

![Testar uma resposta personalizada](images/chatbot-answer-test.png)

--- /task ---

Testa o teu código outra vez. Observa que a resposta que digitas é armazenada no `nome`{:class="block3variables"} e também é mostrada no canto superior esquerdo do palco. Para o fazer desaparecer do Palco, vai à secçāo de blocos `Variáveis`{:class="block3variables"} e clica na caixa ao lado de `nome`{:class="block3variables"} para que não esteja marcado.