# Step 3: Making decisions

You can program your ChatBot to decide what to do, based on the user's responses.

+ Ask the user another question "Are you OK?", and code your ChatBot to reply "That's great to hear!" only __if__ the user answers "yes".

    Test and save: To test your new code properly, you should test it __twice__, once answering "yes", and once answering "no".

    Your ChatBot should reply "That's great to hear!" if you answer "yes", but say nothing if you answer "no".

    ![screenshot](images/chatbot-if-test.png)

### Hint 1
{: .hint-heading #hint-1 }
After your ChatBot has said hello, it should now also __ask__ "Are you OK?". __If__ the user answers "yes" then the ChatBot should __say__ "That's great to hear!".
{: .hint-content .hint-1 }

### Hint 2
{: .hint-heading #hint-2 }
Here are the extra code blocks you'll need:
![screenshot](images/chatbot-if-blocks.png)
{: .hint-content .hint-2 }

### Hint 3
{: .hint-heading #hint-3 }
Here's how your code should look:
![screenshot](images/chatbot-if-code.png)
{: .hint-content .hint-3 }

+ The trouble with your chatbot is that it doesn't give a reply if the user answers "no". Can you change your ChatBot so that it also replies "Oh no!" if you answer "no" to the question?

    Test and save: Your ChatBot should now say "Oh no!" if you answer "no". In fact, it will say "On no!" if you answer with anything other than "yes" (the __else__ in an if/else block means __otherwise__).

    ![screenshot](images/chatbot-if-else-test.png)

### Hint 1
{: .hint-heading #hint-1 }
Your ChatBot should now say "That's great to hear!" __If__ the user answers "yes", but should say "Oh no!" if the user answers something __else__.
{: .hint-content .hint-1 }

### Hint 2
{: .hint-heading #hint-2 }
Here are the code blocks you'll need to use:
![screenshot](images/chatbot-if-else-blocks.png)
{: .hint-content .hint-2 }

### Hint 3
{: .hint-heading #hint-3 }
Here's how your code should look:
![screenshot](images/chatbot-if-else-code.png)
{: .hint-content .hint-3 }

+ You can put any code inside an `if` or `else` block, not just code to make your chatbot speak. Can you change the ChatBot's costume to match the response?

    Test and save: You should see your ChatBot's face change, depending on the user's answer.

    ![screenshot](images/chatbot-costume-test.png)

### Hint 1
{: .hint-heading #hint-1 }
Your ChatBot should now also __switch costume__ depending on the answer given.
{: .hint-content .hint-1 }

### Hint 2
{: .hint-heading #hint-2 }
Here are the code blocks you'll need to use:
![screenshot](images/chatbot-costume-blocks.png)
{: .hint-content .hint-2 }

### Hint 3
{: .hint-heading #hint-3 }
Here's how your code should look:
![screenshot](images/chatbot-costume-code.png)
{: .hint-content .hint-3 }

## Challenge: More decisions { .challenge }

Program your chatbot to ask another question - something with a "yes" or "no" answer. Can you make your ChatBot respond to the answer?

![screenshot](images/chatbot-joke.png)
