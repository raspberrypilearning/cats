## Ακολούθησε τις γραμμές

Ίσως παρατηρήσεις ότι, αν σχεδιάσεις μια χαμηλή γέφυρα ανάμεσα στις δύο πλατφόρμες ή μια γραμμή που κλίνει προς τα πάνω, οι γάτες καταλήγουν να βαδίζουν στην πλατφόρμα και όχι πάνω από αυτές!

![Οι γάτες που περπατούν μέσω της πλατφόρμας](images/cat-walk-through-platform.png)

\--- task \---

Στον κώδικα για το αντικείμενο γάτας, πρόσθεσε άλλον ένα βρόχο πριν από το μπλοκ `επόμενη ενδυμασία`{:class="block3looks"}. Αυτή τη φορά, ο βρόχος θα πει στη γάτα να κινηθεί προς τα πάνω κατά `2` έως ότου δεν αγγίζει το μπλε.

![Αντικείμενο γάτας](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Η γάτα θα πρέπει να `κινηθεί προς τα πάνω κατά 2`{:class="block3motion"} `επανειλημμένα μέχρι`{:class="block3control"} να `μην`{:class="block3operators"} `αγγίζει μπλε`{:class="block3sensing "}.

\--- /hint \---

\--- hint \---

Εδώ είναι τα μπλοκ κώδικα που χρειάζεσαι:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

Έτσι πρέπει να μοιάζει ο κώδικας:

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

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Κάνε κλικ στην πράσινη σημαία και δοκίμασε να σχεδιάσεις μια γραμμή που να κλίνει προς τα πάνω. Έλεγξε ότι η γάτα σου ακολουθεί αυτή τη γραμμή.

\--- /task \---