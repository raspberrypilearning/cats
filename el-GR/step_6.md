## Οδήγησέ τους στην ασφάλεια

Το αντικείμενο του παιχνιδιού είναι να καθοδηγήσεις τις γάτες στην ασφάλεια δημιουργώντας ένα μονοπάτι ώστε να φτάσουν στην πόρτα. Δημιούργησε μια μεταβλητή βαθμολογίας για να παρακολουθείς πόσες γάτες φτάνουν στην πόρτα.

--- task ---

Δημιούργησε μια μεταβλητή με το όνομα `βαθμολογία`{:class="block3variables"}.

![Αντικείμενο γάτας](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Πρόσθεσε κώδικα στο αντικείμενο της γάτας σου για να προσθέσεις `1` στη `βαθμολογία`{:class="block3variables"} κάθε φορά που μια γάτα φτάνει στην πόρτα. Επίσης, όρισε τη `βαθμολογία`{:class="block3variables"} στην τιμή `0` `όταν πατηθεί η σημαία`{:class="block3events"} στην αρχή του παιχνιδιού.

![Αντικείμενο γάτας](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Αν`{:class="block3control"} η γάτα `αγγίξει το αντικείμενο της πόρτας`{:class="block3sensing"}, τότε `πρόσθεσε 1 στη βαθμολογία`{:class="block3variables"}.

--- /hint ---

--- hint ---

Εδώ είναι τα νέα μπλοκ κώδικα που πρέπει να προσθέσεις στο μέρος του προγράμματος `όταν ξεκινώ ως κλώνος`:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

--- /hint ---

--- hint ---

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

Πρόσθεσε κι άλλο κώδικα έτσι ώστε, όταν ένα αντικείμενο γάτας φτάσει στην πόρτα, η γάτα κάνει έναν ήχο «νιάου» και στη συνέχεια εξαφανίζεται.

![Αντικείμενο γάτας](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---