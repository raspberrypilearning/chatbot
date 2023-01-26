## Mudando de lugar

Você também pode programar seu chatbot para alterar sua localização!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

\--- task \---

Você pode programar seu chatbot para perguntar "Você quer ir à lua" e, em seguida, alterar o pano de fundo quando a resposta for "sim"?

\--- dica \---

\--- hint \---

O seu robô deve `perguntar "Você quer ir à lua"`{:class="block3sensing"}, e `se`{:class="block3control"} a `resposta`{:class="block3sensing"} for "sim", deve `mudar o cenário para a lua`{:class="block3look"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos de código que você precisa adicionar ao seu código do chatbot.

![ator nano](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

É assim que seu código deve ser:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Agora você precisa ter certeza de que seu chatbot começa no local certo quando você clicar nele para falar com ele. Adicione este bloco no topo do seu código do chatbot:

![ator nano](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Teste seu programa e responda "sim" quando o chatbot pergunta se você quer ir à lua. Você deve ver que a localização do chatbot muda.

\--- /task \---

\--- task \---

Você também pode adicionar o seguinte código dentro do novo bloco `se`{:class="block3control"} para fazer o chatbot saltar e descer quatro vezes se você responder "sim":

![ator nano](images/nano-sprite.png)

```blocks3
if <(answer) = [yes]> then 
  switch backdrop to (moon v)

+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

\--- /task \---