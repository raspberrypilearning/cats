## बिल्लियों को चलाएँ

एक बार जब बिल्ली फर्श पर पहुँच जाती है, तो उसे धीरे-धीरे दाईं ओर जाना चाहिए।

--- task ---

`when I start as a clone`{:class="block3control"} खाने में कोड जोड़े जिससे cat स्प्राइट `move ten steps`{:class="block3motion"}, और स्प्राइट के दोनों कॉस्ट्यूम (costumes) को हर 0.1 सेकंड में बदले जिससे यह लगे की बिल्ली चल रही हैं।

![Cat sprite](images/cat-sprite.png)

--- hints ---
 --- hint ---

बिल्ली स्प्राइट (cat sprite) को चलाने के लिए `move 10 steps`{:class="block3motion"}, और हर `0.1 seconds`{:class="block3control"} पर कॉस्ट्यूम/पोशाक (costume) बदलने के लिए `switch costume`{:class="block3looks"} का उपयोग करें। इस कोड को भी `forever`{:class="block3control"} दोहराना चाहिए, बिल्ली को गिराने वाले कोड की तरह।

--- /hint ---

--- hint ---

आपको इन कोड ब्लॉक की ज़रुरत पड़ेगी:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

--- /hint ---

--- hint ---

आपका कोड कुछ ऐसा दिखना चाहिए:

```blocks3
when I start as a clone
show
+ forever
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

हरे झंडे को दबाएँ और जाँचें कि बिल्लियाँ अब नीचे नीले मंच के साथ चलती हैं।

--- /task ---

यदि आप खाली जगह पर पुल बनाते हैं ताकि बिल्लियाँ स्टेज के दाईं ओर पूरे रास्ते पर चल सकें, तो आप देख सकते हैं कि वे अंत में दाहिनी दीवार में जाकर अटक जाती हैं।

![Flailing cats at the edge](images/flailing-at-edge.png)

--- task ---

`forever`{:class="block3control"} लूप (loop) को निकालें, और इसके बजाय एक अलग लूप जोड़ें जिससे बिल्लियां केवल तब तक चले जब तक वे किसी किनारे पर नहीं पहुँच जातीं। जब कोई बिल्ली स्टेज के किनारे पर पहुँच जाती है, तो उसे गायब हो जाना चाहिए।

![Cat sprite](images/cat-sprite.png)

```blocks3
when I start as a clone
show
+ repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
+ delete this clone
```

--- /task ---

--- task ---

हरे झंडे को दबाएं और जांचें कि जब वे स्टेज के किनारे तक पहुंचते हैं तो बिल्लियां गायब हो जाती हैं।

--- /task ---

आप देख सकते हैं कि, यदि बिल्लियाँ छेद में गिरती हैं, तो वे गायब नहीं होती हैं, बल्कि नीचे तल में अटक जाती हैं। ऐसा इसलिए है क्योंकि वे नीचे की तरफ गिरने की कोशिश करती रहती हैं।

यह उस कोड का हिस्सा है जो बिल्ली को बताता है कि वह तब तक गिरती रहे जब तक कि वह नीले रंग को नहीं छू लेती:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

हालांकि, छेद में, बिल्ली कभी भी नीले रंग तक नहीं पहुँच सकती, इसलिए यह हमेशा के लिए अटक जाती है।

--- task ---

इस लूप में अधिक ब्लॉक जोड़ें, ताकि यह तब तक दोहराता रहे जब तक कि बिल्ली स्प्राइट नीले रंग को न छू ले, `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"} का उपयोग करें। इस तरह, स्प्राइट अगर स्टेज के किनारे तक पहुँच जाता है तो वह गिरने की कोशिश करना बंद कर देता है।

![Cat sprite](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

--- /task ---