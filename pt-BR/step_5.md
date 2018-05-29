## Etapa 3: Tomando decisões

Você pode programar o seu chatbot para decidir o que dizer ou fazer com base nas suas respostas às suas perguntas.

\--- task \---

Você pode fazer o chatbot fazer a pergunta "Você está bem?", e codificá-lo para responder "Que bom ouvir isso!" somente **se** o usuário responder "sim"?

Para testar o seu novo código corretamente, você deve testá-lo **duas vezes**, uma vez com a resposta "sim" e uma vez com a resposta "não".

Seu chatbot deve responder "Que bom ouvir isso!" se você responder "sim", mas não diga nada se você responder "não".

![Testando uma resposta do chatbot](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- Após o seu chatbot ter dito "Oi", agora também deve **perguntar** "Você está bem?". **se** você responder "sim", então o chatbot deve **dizer** "Que bom ouvir isso!". \--- /hint \--- \--- hint \--- Aqui estão os blocos de código que você precisará: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- Isto é como seu código deve se parecer: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

No momento, o seu chatbot não diz nada se você responder "não". Você pode mudar seu chatbot para que ele também responda "Ah não!" se você responder "não" à sua pergunta?

Teste e salve. Seu chatbot agora deve dizer "Ah não!" se você responder "não". Na verdade, ele vai dizer "Ah não!" se você responder com algo diferente de "sim" (o **então** em um bloco `se/então` significa **caso contrário**).

![Testando uma resposta sim/não](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- seu chatbot agora deve dizer "Que bom ouvir isso!" **se** sua resposta for "Sim", mas deveria dizer "Ah não!" se você responder **qualquer outra coisa**. \--- /hint \--- \--- hint \--- Aqui estão os blocos de código que você precisará: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Isto é como seu código deve se parecer: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Você pode colocar qualquer código dentro de um bloco `if/else`, não apenas código para fazer seu chatbot falar. Se você clicar em guia de **fantasia** do seu chatbot, você verá que ele tem mais de um traje.

![trajes de chatbot](images/chatbot-costume-view.png)

\--- /task \---

\--- task \---

Você pode mudar o traje do chatbot para coincidir com a sua resposta?

Teste e salve. Você deve ver o rosto do seu chatbot mudar dependendo de sua resposta.

![Testando mudança de traje](images/chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Seu chatbot deve agora também ** trocar de traje** dependendo da resposta dada. \--- /hint \--- \--- hint \--- Aqui estão os blocos de código que você precisará: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- /hint \--- \--- hint \--- Isto é como seu código deve se parecer: ![Code for a changing costume](images/chatbot-costume-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Você notou que o traje do seu chatbot permanece o mesmo que mudou desde a última vez que falou com ele? Você pode corrigir esse problema?

![Bug do traje](images/chatbot-costume-bug-test.png)

Teste e salve: execute seu código e digite "não", para que seu chatbot pareça infeliz. Quando você executar novamente o seu código, seu chatbot deve mudar para uma face sorridente antes de perguntar seu nome.

![Testando o conserto do traje](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- Quando o ** sprite é clicado**, seu chatbot deve primeiro **trocar de traje** para um rosto feliz. \--- /hint \--- \--- hint \--- Aqui estão os blocos de código que você precisará: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- /hint \--- \--- hint \--- Isto é como seu código deve se parecer: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Desafio: mais decisões

Programa seu chatbot para responder a outra pergunta - alguma coisa com "sim" ou "não" como resposta. Você pode fazer seu chatbot reagir à resposta?

![captura de tela](images/chatbot-joke.png) \--- /challenge \---