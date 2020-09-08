## স্থান পরিবর্তন করা

আপনি আপনার Chatbot টিকে অবস্থান পরিবর্তন করতে প্রোগ্রামও করতে পারেন!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

--- task ---

আপনি কি আপনার chatbot টিকে "Do you want to go to the moon" জিজ্ঞাসা করার জন্য প্রোগ্রাম করতে পারেন, এবং তারপরে উত্তর "yes" হলে ব্যাক ড্রপ পরিবর্তন করতে পারেন?

--- hints ---


--- hint ---

আপনার চ্যাটবট এর উচিত `ask "Do you want to go to the moon?"`{:class="block3sensing"}, এবং `if`{:class="block3control"} আপনার`answer`{:class="block3sensing"} "yes", এটি হওয়া উচিত`switch the backdrop to the moon`{:class="block3looks"}.

--- /hint ---

--- hint ---

আপনার chatbot code টিতে আপনার যে code block গুলি যুক্ত করতে হবে তা এখানে।.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

--- /hint ---

--- hint ---

আপনার Code টি দেখতে এমন হওয়া উচিত:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

এখন আপনি এটি নিশ্চিত করতে হবে যে আপনি যখন কথা বলার জন্য এটিতে ক্লিক করেন তখন আপনার chatbot টি সঠিক স্থানে শুরু হয়। আপনার chatbot code এর শীর্ষে এই block টি যুক্ত করুন:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

--- /task ---

--- task ---

আপনার প্রোগ্রামটি পরীক্ষা করুন এবং চ্যাটবোটটি চাঁদে যেতে চাইলে জিজ্ঞাসা করলে "yes" উত্তর দিন। আপনার চ্যাটবটের অবস্থান পরিবর্তন দেখতে পাওয়া উচিত।.

--- /task ---

--- task ---

আপনি যদি "yes" এর উত্তর দেন তাহলে chatbot টিকে চারবার লাফিয়ে লাফিয়ে তুলতে, নতুন `if`{:class="block3control"}ব্লকটির ভিতরে নীচের কোডটি যুক্ত করতে পারেন:

![nano sprite](images/nano-sprite.png)

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

--- /task ---