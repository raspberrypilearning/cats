## सुरक्षित रहें

गेम का उद्देश्य एक रास्ता बनाकर बिल्लियों को सुरक्षित मार्गदर्शन करना है ताकि वे दरवाजे तक पहुँच सकें। दरवाजे तक कितनी बिल्लियाँ पहुँचती हैं, इस पर नज़र रखने के लिए एक स्कोर वेरिएबल (score variable) बनाएँ।

--- task ---

`score`{:class="block3variables"} नामक एक वेरिएबल (variable) बनाएं |

![Cat sprite](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

हर बार जब कोई बिल्ली दरवाजे तक पहुँचती है तो `score`{:class="block3variables"} में `1` जोड़ने के लिए अपने बिल्ली स्प्राइट में कोड जोड़ें। साथ ही गेम के आरंभ में `when the flag is clicked`{:class="block3events"} में `score`{:class="block3variables"} को `0` सेट करें।

![Cat sprite](images/cat-sprite.png)

--- hints ---
 --- hint ---

यदि बिल्ली दरवाजा स्प्राइट को छूती है तो उपयोग करें `If`{:class="block3control"} the cat is `touching the door sprite`{:class="block3sensing"}, फिर जोड़ें `add 1 to the score`{:class="block3variables"}।

--- /hint ---

--- hint ---

यहाँ नए कोड ब्लॉक दिए गए हैं जिन्हें आपको अपनी `when I start as a clone` स्क्रिप्ट में जोड़ने की आवश्यकता होगी:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

--- /hint ---

--- hint ---

आपका कोड ऐसा दिखना चाहिए:

```blocks3
when I start as a clone
show
repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    repeat until <not <touching color [#0000ff]?>>
        change y by (2)
    end
    next costume
    wait (0.1) seconds
+   if <touching (Door v)?> then
        change [score v] by (1)
    end
end
delete this clone

when flag clicked

+ set [score v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

कुछ और कोड जोड़ें ताकि जब बिल्ली स्प्राइट दरवाजे तक पहुँच जाए, तो बिल्ली 'म्याऊँ' ('meow') की आवाज करे और फिर गायब होजाए।

![Cat sprite](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---