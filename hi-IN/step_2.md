## रेखाएँ खींचें

\--- task \---

'CATS!' Scratch स्टार्टर प्रोजेक्ट खोलें।

**ऑनलाइन:** [rpf.io/cats-on](http://rpf.io/cats-on){:target="_blank"} पर स्टार्टर प्रोजेक्ट खोलें।

अगर आपके पास एक Scratch अकाउंट है तो आप एक कॉपी **Remix** क्लिक कर के भी बना सकते है।

**ऑफ़लाइन:** ऑफ़लाइन एडिटर में [स्टार्टर प्रोजेक्ट](http://rpf.io/p/en/cats-go) खोलें। यदि आपको Scratch ऑफ़लाइन एडिटर को डाउनलोड और इंस्टॉल करने की आवश्यकता है, तो आप इसे [rpf.io/scratchoff](http://rpf.io/scratchoff) {:target="_blank"} पर प्राप्त कर सकते हैं।

\--- /task \---

\--- task \---

अपने परियोजना में पेन एक्सटेंशन जोड़ें।

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

'पेन' नामक sprite पर क्लिक करें, और स्टेज पर मौजूद बाधाओं के समान पेन का रंग नीला सेट करने के लिए कोड जोड़ें।

![पेन स्प्राइट](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

किसी रंग को चुनने के लिए, `set pen color`{:class="block3extensions"} ब्लॉक में रंग वर्ग पर क्लिक करके आपके माउस कर्सर को पिपेट (नलिका) में बदलें, और फिर स्टेज पर सही रंग पर क्लिक करें।

\--- /task \---

\--- task \---

स्प्राइट द्वारा माउस पॉइंटर का अनुसरण करने के लिए कुछ और कोड जोड़ें। कोड काम करता है यह जाँचने के लिए अपने प्रोग्राम का परीक्षण करें।

![पेन स्प्राइट](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Add some code to tell the sprite to draw a line on the Stage if the mouse button is pressed down.

![पेन स्प्राइट](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`If`{:class="block3control"} the `mouse is down`{:class="block3sensing"}, put the `pen down`{:class="block3extensions"}, and `else`{:class="block3control"}, lift the `pen up`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

यहाँ मौजूद कोड ब्लॉक की आपको जरुरत पड़ेगी:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

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

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। You should be able to click and drag with the mouse to draw a blue line on the Stage.

![एक रेखा खींचें](images/draw-a-line.png)

\--- /task \---

You probably see that a blue dot always appears in the top right-hand corner of the Stage (it's circled in the image above). This is because, when you click the green flag to start the game, you press the mouse down, and so the pen immediately starts drawing.

\--- task \---

To stop this from happening, add a `pen up`{:class="block3extensions"} block at the start of the script, and a `wait one second`{:class="block3control"} block above the `forever`{:class="block3control"} block.

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

\--- /task \---