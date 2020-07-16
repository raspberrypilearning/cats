## बिल्लियाँ को क्लोन (clone) करना

आप बिल्लियों की एक कभी न खत्म होने वाली धारा चाहते हैं। खिलाड़ी को बिल्लियों को बाहर निकालने के लिए मार्गदर्शन देना होगा।

\--- task \---

'Cat' नामक स्प्राइट पर क्लिक करें, और कुछ कोड जोड़े, जिससे वो `hide`{:class="block3looks"} जाए और हर तीन सेकंड में वो `clone`{:class="block3control"} होता रहें।

![Cat sprite](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

यदि आप अब प्रोग्राम चलाते हैं, तो स्टेज पर कुछ भी नहीं होगा। यह जाँचने के लिए कि हर तीन सेकंड में एक नया Cat स्प्राइट का क्लोन बनता है, प्रत्येक क्लोन को आसमान से प्रकट होता हुआ और गिरता हुआ दिखाएँ।

\--- task \---

स्प्राइट में कोड जोड़ें जिससे उसे पता चले कि `when it starts as a clone`{:class="block3control"} के रूप में शुरू होता है, तो यह खुद से `show`{:class="block3looks"} देना चाहिए और तब तक गिरना चाहिए जब तक कि यह स्टेज पर खींची गई नीली मंजिल को `touches`{:class="block3sensing"} हैं।

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`When the sprite starts as a clone`{:class="block3control"}, `show`{:class="block3looks"} वह स्प्राइट | `Repeatedly`{:class="block3control"} `Change`{:class="block3motion"} करें स्प्राइट के `y` निर्देशांक (coordinates) `-2` से जब तक स्प्राइट नीली मंजिल को `touches`{:class="block3sensing"} न लें |

\--- /hint \---

\--- hint \---

आपको इन कोड ब्लॉक्स की ज़रुरत पड़ेगी:

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

\--- /hint \---

\--- hint \---

आपका कोड कुछ ऐसा दिखना चाहिए:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

जब आप हरे झंडे पर क्लिक करते हैं, तो आपको हर तीन सेकंड में स्टेज के ऊपर से एक नई बिल्ली गिरती हुई दिखाई देनी चाहिए। प्रत्येक बिल्ली को नीचे की नीली मंजिल पर एक के ऊपर एक गिरे हुए बिल्लियों के बड़े ढेर में उतरना चाहिए।

![Falling cats](images/falling-cats.png)