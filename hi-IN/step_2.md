## रेखाएँ खींचें

--- task ---

'CATS!' Scratch स्टार्टर प्रोजेक्ट खोलें।

**ऑनलाइन:** [rpf.io/cats-on](https://rpf.io/cats-on){:target="_blank"} पर स्टार्टर प्रोजेक्ट खोलें।

अगर आपके पास एक Scratch अकाउंट है तो आप एक कॉपी **Remix** क्लिक कर के भी बना सकते है।

**ऑफ़लाइन:** ऑफ़लाइन एडिटर में [स्टार्टर प्रोजेक्ट](https://rpf.io/p/hi-IN/cats-go) खोलें। यदि आपको Scratch ऑफ़लाइन एडिटर को डाउनलोड और इंस्टॉल करने की आवश्यकता है, तो आप इसे [rpf.io/scratchoff](https://rpf.io/scratchoff) {:target="_blank"} पर प्राप्त कर सकते हैं।

--- /task ---

--- task ---

अपने परियोजना में पेन एक्सटेंशन जोड़ें।

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

'पेन' नामक sprite पर क्लिक करें, और स्टेज पर मौजूद बाधाओं के समान पेन का रंग नीला सेट करने के लिए कोड जोड़ें।

![पेन स्प्राइट](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

किसी रंग को चुनने के लिए, `set pen color`{:class="block3extensions"} ब्लॉक में रंग वर्ग पर क्लिक करके आपके माउस कर्सर को पिपेट (नलिका) में बदलें, और फिर स्टेज पर सही रंग पर क्लिक करें।

--- /task ---

--- task ---

स्प्राइट द्वारा माउस पॉइंटर का अनुसरण करने के लिए कुछ और कोड जोड़ें। कोड काम करता है यह जाँचने के लिए अपने प्रोग्राम का परीक्षण करें।

![पेन स्प्राइट](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

यदि माउस बटन नीचे दबाया जाता है तो स्टेज पर एक रेखा खींचने के लिए स्प्राइट को बताने के लिए कुछ कोड जोड़ें।

![पेन स्प्राइट](images/pen-sprite.png)

--- hints ---
 --- hint ---

`If`{:class="block3control"} the `mouse is down`{:class="block3sensing"}, `pen down`{:class="block3extensions"} रखें, और `else`{:class="block3control"}, `pen up`{:class="block3extensions"} रखें।

--- /hint ---

--- hint ---

यहाँ मौजूद कोड ब्लॉक की आपको जरुरत पड़ेगी:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

आपका कोड ऐसा दिखना चाहिए:

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

अपने कोड का परीक्षण करें। आप माउस से क्लिक और ड्रैग (drag) करके स्टेज पर नीली रेखा खींच पाएँगे।

![एक रेखा खींचें](images/draw-a-line.png)

--- /task ---

आप शायद यह देखेंगे कि स्टेज के ऊपरी दाएँ कोने में एक नीली बिंदू हमेशा दिखाई देती है (ऊपर की छवि में इस पर घेरा डाला गया है)। ऐसा इसलिए है क्योंकि जब आप गेम शुरू करने के लिए हरे झंडे पर क्लिक करते हैं, तो आप माउस को नीचे दबाते हैं, और इसलिए पेन तुरंत बनाना शुरू कर देता है।

--- task ---

ऐसा होने से रोकने के लिए, स्क्रिप्ट के आरंभ में एक `pen up`{:class="block3extensions"} ब्लॉक जोड़ें, और `forever`{:class="block3control"} ब्लॉक के ऊपर एक `wait one second`{:class="block3control"} ब्लॉक को जोड़ें।

![पेन स्प्राइट](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

--- /task ---
