## تغيير المكان

يمكنك أيضًا برمجة روبوتك ليغيِّر مكانه!

![اختبار تغيير الخلفية](images/chatbot-backdrop-moon.png)

--- task ---

هل يمكنك برمجة روبوتك ليسأل "هل تود الصعود إلى سطح القمر؟" ثم يغيِّر مكانه إذا كانت إجابتك هي "نعم"؟

--- hints ---


--- hint ---

يجب أن يسأل روبوتك `"هل تريد الذهاب إلى القمر؟"`{:class="block3sensing"} ، و `إذا`{:class="block3control"} كانت `الإجابة`{:class="block3sensing"} "نعم" ، يجب أن `تتبدل الخلفية إلى القمر`{:class="block3looks"}.

--- /hint ---

--- hint ---

فيما يلي الكتل البرمجية التي تحتاج إلى إضافتها إلى روبوت الدردشة الخاصة بك.

![كائن نانو](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [هل ترغب بالذهاب الى القمر؟] and wait

if <(الإجابة) = [نعم]> then 

end
```

--- /hint ---

--- hint ---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

```blocks3
ask [هل ترغب بالذخاب الى القمر؟] and wait
if <(الإجابة) = [نعم]> then 
  switch backdrop to (moon v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

تحتاج الآن إلى التأكد من أن الروبوت يبدأ في الموقع الصحيح عند النقر فوقه للتحدث إليه. أضف هذه الكتلة إلى أعلى التعليمات البرمجية للروبوت:

![كائن نانو](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch backdrop to (space v)
```

--- /task ---

--- task ---

اختبر برنامجك، أجب بـ"نعم" عندما يسألك الروبوت هل ترعب بالذهاب الى القمر. يجب أن ترى موقع الروبوت يتغير.

--- /task ---

--- task ---

يمكنك أيضًا إضافة الكود التالي داخل `اذا`{:class="block3control"} الجديدة لجعل الروبوت يقفز لأعلى ولأسفل أربع مرات إذا أجبت "نعم":

![كائن نانو](images/nano-sprite.png)

```blocks3
if <(الإجابة) = [نعم]> then 
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