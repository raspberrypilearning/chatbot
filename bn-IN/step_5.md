## সিদ্ধান্ত গ্রহণ করছি

যে উত্তরগুলি পেয়েছে তার উপর ভিত্তি করে কী করবে তা সিদ্ধান্ত নিতে আপনি আপনার চ্যাটবটকে প্রোগ্রাম করতে পারেন।.

প্রথমত, আপনি আপনার চ্যাটবোটকে এমন প্রশ্ন জিজ্ঞাসা করতে যাচ্ছেন যা "yes" বা "no" দিয়ে উত্তর দেওয়া যেতে পারে।.

--- task ---

আপনার চ্যাটবোটের কোডটি পরিবর্তন করুন।. আপনার চ্যাটবোটটির `name`{:class="block3variables"} ভেরিয়েবল ব্যবহার করে "Are you OK name", প্রশ্নটি জিজ্ঞাসা করা উচিত।. তারপরে এটির উত্তর দেওয়া উচিত "That's great to hear!" `if`{:class="block3control"} উত্তরটি হয় "yes", তবে উত্তরটি যদি"no" হয় তবে কিছু বলবেন ।.

![Testing a chatbot reply](images/chatbot-if-test1-annotated.png)

![Testing a chatbot reply](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
end
```

আপনার নতুন কোডটি সঠিকভাবে পরীক্ষা করতে, আপনার এটি **twice**: বার পরীক্ষা করা উচিত: একবার "yes" উত্তরের সাথে এবং একবার "no" উত্তর দিয়ে।.

--- /task ---

এই মুহুর্তে, আপনার চ্যাটবোট "no" উত্তরে কিছু বলে না।.

--- task ---

আপনার চ্যাটবটের কোডটি এমন পরিবর্তন করুন যাতে এটি "Oh no!!" রিপ্লাই করে যদি এটি "Are you OK name". এর উত্তর হিসাবে "no" পায়।.

`if, then`{:class="block3control"} ব্লক টিকে `if, then, else`{:class="block3control"} এ প্রতিস্থাপন করুন, এবং তারপরে কোড অন্তর্ভুক্ত করুন যাতে চ্যাটবট বলতে পারে `say "Oh no!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait

+ if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
else 
+  say [Oh no!] for (2) seconds
end
```

--- /task ---

--- task ---

আপনার কোড পরীক্ষা করুন।. আপনি "no" জবাব দেওয়ার সময় এবং "yes" জবাব দেওয়ার সময় আপনার আলাদা প্রতিক্রিয়া পাওয়া উচিত: আপনার চ্যাটবোটটিতে That’s great to hear!" যখন আপনি "yes" (যা কেস-সংবেদনশীল নয়) এর উত্তর দেন এবং "Oh no!"আপনি যখন উত্তর দিবেন **anything else**.

![Testing a chatbot reply](images/chatbot-if-test2.png)

![Testing a yes/no reply](images/chatbot-if-else-test.png)

--- /task ---

আপনি কোনও কোড `if, then, else`{:class="block3control"} ব্লক এর ভিতরে রাখতে পারেন, কেবল আপনার চ্যাটবোটকে কথা বলার জন্য কোড নয়!

আপনি যদি আপনার চ্যাটবটের **Costumes** ট্যাবে ক্লিক করেন তবে দেখতে পাবেন যে একাধিক costume রয়েছে।.

![chatbot costumes](images/chatbot-costume-view-annotated.png)

--- task ---

আপনার চ্যাটবটের কোডটি এমন পরিবর্তন করুন যাতে আপনি উত্তরটিতে টাইপ করার সময় চ্যাটবট costumes এ স্যুইচ করে।.

![Testing a changing costume](images/chatbot-costume-test1.png)

![Testing a changing costume](images/chatbot-costume-test2.png)

`if, then, else`{:class="block3control"} ব্লক এর অভ্যন্তরে কোডটি পরিবর্তন করে এটি `switch costume`{:class="block3looks"}.করুন.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 

+  switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
```

আপনার Code টি পরীক্ষা এবং সংরক্ষণ করুন। আপনার উত্তরের উপর নির্ভর করে আপনার Chatbot এর চেহারা পরিবর্তন হওয়া উচিত।.

--- /task ---

আপনি কি লক্ষ্য করেছেন যে আপনার Chatbot এর costume বদলে যাওয়ার পরে, এটি এমনই থাকে এবং এটি শুরুতে যেমন ছিল তেমন ফিরে আসে না?

আপনি এটি চেষ্টা করে দেখতে পারেন: আপনার Code টি run করুন এবং "no" উত্তর দিন যাতে আপনার Chatbot এর মুখটি অসুখী চেহারায় পরিবর্তিত হয়।. তারপরে আপনার Code টি আবার run করুন এবং লক্ষ্য করুন যে আপনার Chatbot টি আপনার নাম জিজ্ঞাসা করার আগে সুখী মুখে ফিরে আসে না।.

![Costume bug](images/chatbot-costume-bug-test.png)

--- task ---

এই সমস্যাটি সমাধান করতে, Chatbot এর Code টিতে `switch costume`{:class="block3looks"} যোগ করুন শুরুতে `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Testing a costume fix](images/chatbot-costume-fix-test.png)

--- /task ---