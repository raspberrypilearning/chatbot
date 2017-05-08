## Step 3: Making decisions

You can program your ChatBot to decide what to say or do, based on the user's responses.

+ Ask the user another question "Are you OK?", and code your ChatBot to reply "That's great to hear!" only __if__ the user answers "yes".

    Test and save: To test your new code properly, you should test it __twice__, once answering "yes", and once answering "no".

    Your ChatBot should reply "That's great to hear!" if you answer "yes", but say nothing if you answer "no".

    ![screenshot](images/chatbot-if-test.png)

--- hints ---
--- hint ---
After your ChatBot has said "Hi", it should now also __ask__ "Are you OK?". __If__ the user answers "yes" then the ChatBot should __say__ "That's great to hear!".
--- /hint ---
--- hint ---
Here are the extra code blocks you'll need:
![screenshot](images/chatbot-if-blocks.png)
--- /hint ---
--- hint ---
Here's how your code should look:
![screenshot](images/chatbot-if-code.png)
--- /hint ---
--- /hints ---

+ The trouble with your chatbot is that it doesn't give a reply if the user answers "no". Can you change your ChatBot so that it also replies "Oh no!" if you answer "no" to the question?

    Test and save: Your ChatBot should now say "Oh no!" if you answer "no". In fact, it will say "On no!" if you answer with anything other than "yes" (the __else__ in an if/else block means __otherwise__).

    ![screenshot](images/chatbot-if-else-test.png)

--- hints ---
--- hint ---
Your ChatBot should now say "That's great to hear!" __If__ the user answers "yes", but should say "Oh no!" if the user answers something __else__.
--- /hint ---
--- hint ---
Here are the code blocks you'll need to use:
![screenshot](images/chatbot-if-else-blocks.png)
--- /hint ---
--- hint ---
Here's how your code should look:
![screenshot](images/chatbot-if-else-code.png)
--- /hint ---
--- /hints ---

+ You can put any code inside an `if` or `else` block, not just code to make your chatbot speak. If you click your ChatBot's 'costume' tab, you'll see that there is more than one.

    ![screenshot](images/chatbot-costume-view.png)

+ Can you change the ChatBot's costume to match the response?

    Test and save: You should see your ChatBot's face change, depending on the user's answer.

    ![screenshot](images/chatbot-costume-test.png)

--- hints ---
--- hint ---
Your ChatBot should now also __switch costume__ depending on the answer given.
--- /hint ---
--- hint ---
Here are the code blocks you'll need to use:
![screenshot](images/chatbot-costume-blocks.png)
--- /hint ---
--- hint ---
Here's how your code should look:
![screenshot](images/chatbot-costume-code.png)
--- /hint ---
--- /hints ---

+ Have you noticed that your ChatBot's costume stays the same as the last time you spoke to it? Can you fix this problem?

    ![screenshot](images/chatbot-costume-bug-test.png)

    Test and save: Run your code and type "no", so that your ChatBot looks unhappy. When you run your code again, your ChatBot should change back to a smiling face before asking your name.

    ![screenshot](images/chatbot-costume-fix-test.png)

--- hints ---
--- hint ---
When the __sprite is clicked__, your ChatBot should first __switch costume__ to a smiling face.
--- /hint ---
--- hint ---
Here's the code block you'll need to add:
![screenshot](images/chatbot-costume-fix-blocks.png)
--- /hint ---
--- hint ---
Here's how your code should look:
![screenshot](images/chatbot-costume-fix-code.png)
--- /hint ---
--- /hints ---

--- challenge ---
## Challenge: More decisions

Program your chatbot to ask another question - something with a "yes" or "no" answer. Can you make your ChatBot respond to the answer?

![screenshot](images/chatbot-joke.png)
--- /challenge ---
