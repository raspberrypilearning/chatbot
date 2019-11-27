## Mudando de lugar

Você também pode programar o seu ChatBot para mudar de lugar!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

\--- task \---

Você pode programar seu chatbot para perguntar "Você quer ir à lua", e então mudar o plano de fundo quando a resposta é "sim"?

\--- dica \---

\--- hint \---

O seu robô deve `perguntar "Você quer ir à lua"`{:class="block3sensing"}, e `se`{:class="block3control"} a `resposta`{:class="block3sensing"} for "sim", deve `mudar o cenário para a lua`{:class="block3look"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos de código que você precisa adicionar ao seu código do chatbot.

![ator nano](images/nano-sprite.png)

```blocks3
muda o cenário para (moon v)

pergunta [Você quer ir à lua] e espera pela resposta

se <(a resposta) = [sim]>, então
end
```

\--- /hint \---

\--- hint \---

É assim que seu código deve ser:

```blocks3
pergunta [Você quer ir à lua?] e espera pela resposta
se <(a resposta) = [sim]>, então 
  muda o cenário para (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Agora você precisa ter certeza de que seu chatbot começa no local certo quando você clicar nele para falar com ele. Adicione este bloco no topo do seu código do chatbot:

![ator nano](images/nano-sprite.png)

```blocks3
quando alguém clicar em você

muda o cenário para (space v)
```

\--- /task \---

\--- task \---

Teste seu programa e responda "sim" quando o chatbot pergunta se você quer ir à lua. Você deve ver que a localização do chatbot muda.

\--- /task \---

\--- task \---

Você também pode adicionar o seguinte código dentro do novo bloco `se`{:class="block3control"} para fazer o chatbot saltar e descer quatro vezes se você responder "sim":

![ator nano](images/nano-sprite.png)

```blocks3
se <(a resposta) = [sim]>, então 
  muda o cenário para (moon v)
  + repete (4) vezes 
      adiciona (10) ao teu y
      espera (0.1) s
      adiciona (-10) ao teu y
      espera (0.1) s
     end
end
```

\--- /task \---