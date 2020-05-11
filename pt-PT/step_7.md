## Mudar de localização

Também podes programar o teu robô para mudar a sua localização!

![Testar uma mudança de cenário](images/chatbot-backdrop-moon.png)

--- task ---

Podes programar o teu robô falante para perguntar "Queres ir à lua?" e, depois mudar de cenário se responderes "sim"?

--- hints ---

--- hint ---

O teu robô deve `perguntar "Queres ir à lua?"`{:class="block3sensing"}, e `se`{:class="block3control"} a `resposta`{:class="block3sensing"} for "sim", deve `mudar o cenário para a lua`{:class="block3look"}.

--- /hint ---

--- hint ---

Aqui estão os blocos que precisas de adicionar ao código do teu robô falante.

![actor nano](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Queres ir à lua?] and wait

if <(answer) = [sim]> then 

end
```

--- /hint ---

--- hint ---

Este é o aspeto que o teu código deve ter:

```blocks3
ask [Queres ir à lua?] and wait
if <(answer) = [sim]> then 
  switch backdrop to (moon v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Agora precisas ter certeza de que o teu robô começa no local certo quando clicares nele para falar. Adiciona este bloco ao topo do teu código do robô falante:

![actor nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch backdrop to (space v)
```

--- /task ---

--- task ---

Testa o teu programa e responde "sim" quando o robô perguntar se queres ir à lua. Deves ver que a localização do robô falante muda.

--- /task ---

--- task ---

Também podes adicionar o seguinte código dentro do novo bloco `se`{:class="block3control"} para fazer o robô saltar para cima e para baixo quatro vezes se responderes "sim":

![actor nano](images/nano-sprite.png)

```blocks3
if <(answer) = [sim]> then 
  switch backdrop to (moon v)
+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

--- /task ---