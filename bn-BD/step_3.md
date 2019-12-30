## একটি কথা বলা চ্যাটবট

এখন আপনি একটি ব্যক্তিত্বের সাথে একটি চ্যাটবোট আছে, আপনি এটি আপনার সাথে কথা বলতে প্রোগ্রাম করতে যাচ্ছি।

\--- task \---

আপনার চ্যাটবোট স্প্রাইটে ক্লিক করুন এবং এটিকে এই কোডটি যোগ করুন যাতে `এটি`{ক্লাস = "ব্লক 3events"} ক্লিক করে, এটি `আপনার নাম`{: class = "block3sensing"} এবং তারপর `বলবে "কী সুদৃশ্য নাম!"`{: শ্রেণী = "ব্লক 3looks"}।

![ন্যানো স্প্রাইট](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

\--- /task \---

\--- /task \---

আপনার কোড পরীক্ষা করার জন্য আপনার চ্যাটবোট উপর ক্লিক করুন। Chatbot আপনার নাম জন্য অনুরোধ, তখন তা বাক্সে পর্যায় নীচে প্রদর্শিত হবে টাইপ করুন, এবং তারপর নীল চিহ্ন ক্লিক করুন, বা Enter <kbd>লিখুন</kbd>।

![একটি চ্যাটবোট প্রতিক্রিয়া পরীক্ষা করা হচ্ছে](images/chatbot-ask-test1.png)

![একটি চ্যাটবোট প্রতিক্রিয়া পরীক্ষা করা হচ্ছে](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

এই মুহুর্তে, আপনার চ্যাটবোট উত্তর দেয় "কী সুন্দর নাম!" প্রতিবার আপনি উত্তর। আপনি চ্যাটবটের প্রতিক্রিয়াটিকে আরও ব্যক্তিগত করে তুলতে পারেন, যাতে প্রতিবার একটি আলাদা নাম টাইপ করা হলে উত্তরটি আলাদা হয়।.

Change the chatbot sprite’s code to `join`{:class="block3operators"} "Hi" with the `answer`{:class="block3sensing"} to the "What's your name?" question, so that the code looks like this:

![ন্যানো স্প্রাইট](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![ব্যক্তিগতকৃত জবাব পরীক্ষা করা হচ্ছে](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

একটি **পরিবর্তনশীল**এ উত্তর সংরক্ষণ করে, আপনি আপনার প্রকল্পের যে কোন জায়গায় এটি ব্যবহার করতে পারেন।

নামের একটি নতুন পরিবর্তনশীল তৈরি করুন `নাম`{: শ্রেণি = "block3variables"}।

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

এখন, আপনার চ্যাটবট স্প্রাইটের কোডটি ` নাম সেট করতে পরিবর্তন করুন ` ।: class = "block3variables"} ` উত্তরের পরিবর্তনশীল ` {: শ্রেণি = "block3sensing"}:

![ন্যানো স্প্রাইট](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

আপনার কোডটি আগের মতোই কাজ করা উচিত: আপনার চ্যাটবটটিতে আপনার টাইপ করা নামটি ব্যবহার করে হাই বলা উচিত।.

![একটি ব্যক্তিগতকৃত উত্তর পরীক্ষা করা](images/chatbot-answer-test.png)

\--- /task \---

আপনার প্রোগ্রামটি আবার পরীক্ষা করুন।. লক্ষ্য করুন যে আপনার টাইপ করা উত্তরটি ` নামে সঞ্চিত আছে ` class: class = "block3variables"} ভেরিয়েবল, এবং স্টেজের উপরের বাম-কোণেও প্রদর্শিত হয়।. এটি পর্যায় থেকে অদৃশ্য হয়ে যেতে, ` ভেরিয়েবলগুলিতে যান ` class: শ্রেণী = "block3variables"} ব্লক বিভাগ এবং ` নামের পাশের বাক্সে ক্লিক করুন ` ।: class = "block3variables"} যাতে এটি চিহ্নিত না হয়।.