## रेखाओं से जुड़े रहें

आप देख सकते हैं कि, यदि आप दो प्लेटफार्मों के बीच एक नीचा पुल बनाते हैं, या ऊपर की ओर ढलान वाली एक रेखा खींचते हैं, तो बिल्लियाँ प्लेटफार्म के ऊपर चलने के बजाय उसमें से निकल कर जाती हैं!

![Cats walking through the platform](images/cat-walk-through-platform.png)

--- task ---

बिल्ली स्प्राइट के कोड में, `next costume`{:class="block3looks"} ब्लॉक से पहले एक और लूप जोड़ें। इस बार लूप को बिल्ली को यह बताना चाहिए कि जब तक वह नीले रंग को न छू ले, तब तक उसे `2` से ऊपर की ओर जाना चाहिए।

![Cat sprite](images/cat-sprite.png)

--- hints ---
 --- hint ---

बिल्ली को बार-बार ऊपर जाना चाहिए `move up 2`{:class="block3motion"} `repeatedly until`{:class="block3control"} जब तक वह नीले रंग को न छू ले `not`{:class="block3operators"} `touching blue`{:class="block3sensing"} का उपयोग करें |

--- /hint ---

--- hint ---

आपको इन कोड ब्लॉक्स की ज़रुरत पड़ेगी:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
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
end
delete this clone
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

हरे झंडे पर क्लिक करें और एक रेखा खींचने की कोशिश करें जिसकी ढलान ऊपर की ओर हो। जाँच करें कि आपकी बिल्ली इस रेखा का अनुसरण (follow) करती है।

--- /task ---