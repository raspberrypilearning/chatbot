## Tomar decisões

Podes programar o teu robô falante para que ele decida o que dizer ou fazer com base nas respostas que recebe.

Primeiro, vais fazer o teu robô fazer uma pergunta que possa ser respondida com "sim" ou "não".

--- task ---

Altera o código do teu robô. O teu robô deve fazer a pergunta "Estás OK nome", usando a variável `nome`{:class="block3variáveis"}. Então, deve responder "Que bom ouvir isso!" `se`{:class="block3control"} a resposta que recebe é "sim", mas não dizer nada se a resposta for "não".

![Testar a resposta do robô falante](images/chatbot-if-test1-annotated.png)

![Testar a resposta do robô falante](images/chatbot-if-test2.png)

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Como te chamas?] and wait
set [nome v] to (answer)
say (join [Olá ] (nome)) for (2) seconds
+ask (join [Estás OK ] (nome)) and wait
+if <(answer) = [Sim]> then 
  say [Que bom ouvir isso!] for (2) seconds
end
```

Para testares o teu novo código devidamente, deves testá-lo **duas vezes**, uma vez com a resposta "sim", e uma vez com a resposta "não".

--- /task ---

De momento, o teu robô não diz nada à resposta "não".

--- task ---

Altera o código do teu robô para que ele responda "Oh não!" se receber "não" como resposta a "Estás OK nome".

Substitue o bloco `se, então`{:class="block3control"} com um `se, então, senão`{:class="block3control"} e inclui código para que o robô possa `dizer "Oh não!"`{:class="block3look"}.

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Como te chamas?] and wait
set [nome v] to (answer)
say (join [Olá ] (nome)) for (2) seconds
ask (join [Estás OK ] (nome)) and wait
+ if <(answer) = [Sim]> then 
  say [Que bom ouvir isso!] for (2) seconds
else 
+  say [Oh nāo!] for (2) seconds
end
```

--- /task ---

--- task ---

Testa o teu código. Deves receber uma resposta diferente ao responderes "não" e ao responderes "sim": o teu robô deve responder com "Que bom ouvir isso!" quando respondes "sim" (que não diferencia maiúsculas de minúsculas) e responder com "Oh não!" quando respondes **outra coisa qualquer**.

![Testar a resposta do robô falante](images/chatbot-if-test2.png)

![Testar uma resposta sim / não](images/chatbot-if-else-test.png)

--- /task ---

Podes colocar qualquer código dentro de um bloco `se, então, senão`{:class="block3control"}, não apenas código para fazer o teu robô falar!

Se clicares no menu **Trajes** do robô falante, verás que tem mais de um traje.

![trajes do robô falante](images/chatbot-costume-view-annotated.png)

--- task ---

Altera o código do teu robô para que mude o traje quando digitares a tua resposta.

![Testar uma mudança de traje](images/chatbot-costume-test1.png)

![Testar uma mudança de traje](images/chatbot-costume-test2.png)

Altera o código dentro do bloco `se, então, senão`{:class="block3control"} para `mudar o traje`{:class="block3look"}.

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Como te chamas?] and wait
set [nome v] to (answer)
say (join [Olá ] (nome)) for (2) seconds
ask (join [Estás OK ] (nome)) and wait
if <(answer) = [Sim]> then 
+  switch costume to (nano-c v)
  say [Que bom ouvir isso!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh nāo!] for (2) seconds
end
```

Testa e guarda o teu código. Deves ver o rosto do teu robô falante mudar de acordo com a tua resposta.

--- /task ---

Reparaste que depois de o traje do robô ter mudado, ele fica assim e não muda para o que estava no início?

Podes tentar isto: executa o teu código e responde "não" para que o teu robô mude de rosto para um visual triste. Em seguida, executa o teu código novamente e descobre que o teu robô não muda para ficar feliz antes de pedir o teu nome.

![Erros do traje](images/chatbot-costume-bug-test.png)

--- task ---

Para resolver este problema, adiciona código para `mudar de traje`{:class="block3look"} no início `quando o actor é clicado`{:class="block3events"}.

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch costume to (nano-a v)
ask [Como te chamas?] and wait
```

![Testar uma correção do traje](images/chatbot-costume-fix-test.png)

--- /task ---