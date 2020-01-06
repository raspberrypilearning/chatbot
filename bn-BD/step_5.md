## সিদ্ধান্ত নেয়া

আপনি এটি প্রাপ্ত উত্তরগুলির উপর ভিত্তি করে কী করতে হবে তা নির্ধারণ করতে আপনার চ্যাটবোট প্রোগ্রাম করতে পারেন।

প্রথম, আপনি আপনার চ্যাটবোটকে একটি প্রশ্ন জিজ্ঞাসা করতে যাচ্ছেন যা "হ্যাঁ" বা "না" দিয়ে উত্তর দেওয়া যেতে পারে।

\--- কাজ \---

আপনার চ্যাটবোট এর কোড পরিবর্তন করুন। `চ্যাট`{: class = "block3variables"} পরিবর্তনশীল ব্যবহার করে আপনার চ্যাটবোটটি "আপনি ঠিক আছেন নামটি" প্রশ্নটি জিজ্ঞাসা করুন। তারপর এটা উত্তর দিতে হবে "এটা শুনতে মহান!" `যদি`{: class = "block3control"} এটি প্রাপ্ত উত্তরটি "হ্যাঁ" হয় তবে উত্তরটি "না" হলে কিছুই বলবেন না।

![একটি চ্যাটবোট উত্তর পরীক্ষা](images/chatbot-if-test1-annotated.png)

![একটি চ্যাটবোট উত্তর পরীক্ষা](images/chatbot-if-test2.png)

![ন্যানো স্প্রাইট](images/nano-sprite.png)

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

আপনার নতুন কোড সঠিকভাবে পরীক্ষা করার জন্য, আপনি এটি পরীক্ষা করা উচিত **দুইবার**: একবার উত্তর সঙ্গে "হ্যাঁ", এবং একবার উত্তর সঙ্গে "না"।

\--- /কাজ \---

এই মুহুর্তে, আপনার চ্যাটবোটটি "না" উত্তরটিতে কিছু বলে না।

\--- কাজ \---

আপনার চ্যাটবোটের কোডটি পরিবর্তন করুন যাতে এটি "ওহ না!" যদি "আপনি ঠিক আছে নাম" এর উত্তর হিসাবে "না" পেয়ে থাকেন।

`প্রতিস্থাপন করুন, তারপর`{: class = "block3control"} `দিয়ে ব্লক করুন, তারপরে, অন্য`{: class = "block3control"} ব্লক করুন এবং কোড অন্তর্ভুক্ত করুন যাতে চ্যাটবট `বলতে পারে "ওহ না!"`{: শ্রেণী = "ব্লক 3looks"}।

![ন্যানো স্প্রাইট](images/nano-sprite.png)

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

\--- /কাজ \---

\--- কাজ \---

আপনার কোড পরীক্ষা করুন। যখন আপনি "না" উত্তর দিবেন এবং যখন আপনি "হ্যাঁ" উত্তর দিবেন তখন আপনাকে আলাদা প্রতিক্রিয়া জানাতে হবে: আপনার চ্যাটবোটটি "এটি শুনে খুব ভাল" এর উত্তর দিতে হবে! যখন আপনি "হ্যাঁ" উত্তর দেন (যা কেস-সংবেদনশীল নয়), এবং "ওহ না!" দিয়ে উত্তর দিন। যখন আপনি **অন্য কিছু উত্তর দিবেন**।

![একটি চ্যাটবোট উত্তর পরীক্ষা](images/chatbot-if-test2.png)

![একটি হ্যাঁ / কোন উত্তর পরীক্ষা](images/chatbot-if-else-test.png)

\--- /কাজ \---

যদি আপনি `কোনও কোড রাখতে পারেন তবে, অন্যথায়`{: class = "block3control"} ব্লক করুন, শুধুমাত্র আপনার চ্যাটবোটকে কথা বলার জন্য নয়!

আপনি যদি আপনার চ্যাটবোটের **পোষাক** ট্যাবটি ক্লিক করেন তবে আপনি দেখতে পাবেন যে একাধিক পরিচ্ছদ রয়েছে।

![চ্যাটবোট পরিধানসমূহ](images/chatbot-costume-view-annotated.png)

\--- কাজ \---

আপনার চ্যাটবোটের কোডটি পরিবর্তন করুন যাতে আপনার উত্তরটি টাইপ করার সময় চ্যাটবোট পোশাকগুলি স্যুইচ করে।

![একটি পরিবর্তন পোশাক পরিদর্শন](images/chatbot-costume-test1.png)

![একটি পরিবর্তন পোশাক পরিদর্শন](images/chatbot-costume-test2.png)

`ভিতরে কোডটি পরিবর্তন করুন, যদি, অন্যথায়`{: class = "block3control"} `সুইচ পরিচ্ছদ`ব্লক করুন: {class = "block3looks"}।

![ন্যানো স্প্রাইট](images/nano-sprite.png)

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

পরীক্ষা এবং আপনার কোড সংরক্ষণ করুন। আপনার উত্তর অনুসারে আপনার চ্যাটবোটের মুখ পরিবর্তন দেখতে হবে।

\--- /কাজ \---

আপনি কি লক্ষ্য করেছেন যে, আপনার চ্যাটবোটের পরিচ্ছদ পরিবর্তিত হওয়ার পরে এটি এভাবেই চলবে এবং শুরুতে যা যা ছিল তা কি তা পরিবর্তন করবে না?

আপনি এটিকে চেষ্টা করতে পারেন: আপনার কোডটি চালান এবং "না" উত্তর দিন যাতে আপনার চ্যাটবোটের মুখ একটি অসুখী চেহারায় পরিবর্তিত হয়। তারপরে আপনার কোডটি আবার চালান এবং লক্ষ্য করুন যে আপনার চ্যাটবোটটি আপনার নাম জিজ্ঞাসা করার আগে খুশি খুঁজছেন না।

![কস্টিউম বাগ](images/chatbot-costume-bug-test.png)

\--- কাজ \---

এই সমস্যা সমাধানের জন্য, এর chatbot এর কোড যোগ `সুইচ পরিচ্ছদ`{: শ্রেণি = "block3looks"} শুরুতে `যখন পরী ক্লিক না`{: শ্রেণি = "block3events"}।

![ন্যানো স্প্রাইট](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![একটি পরিচ্ছদ ফিক্স পরীক্ষা](images/chatbot-costume-fix-test.png)

\--- /কাজ \---