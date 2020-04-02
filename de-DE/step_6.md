## In Sicherheit bringen

Ziel des Spiels ist es, die Katzen in Sicherheit zu bringen, indem ein Pfad erstellt wird, über den sie die Tür erreichen können. Erstelle eine Punktevariable, um den Überblick zu behalten, wie viele Katzen die Tür erreichen.

--- task ---

Erstelle eine neue Variable namens `Punktzahl`{:class='block3variable'}.

![Katzen Figur](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Füge deiner Katzen-Figur Code hinzu, um jedesmal `1` zur `Punktzahl`{:class="block3variables"} hinzuzufügen, wenn eine Katze die Tür erreicht. Setze außerdem die `Punktzahl`{:class="block3variables"} beim Start des Spiels auf `0` `wenn die grüne Flagge angeklickt wird`{:class="block3events"}.

![Katzen Figur](images/cat-sprite.png)

--- hints --- --- hint ---

`Falls`{:class="block3control"} die Katze `die Tür berührt`{:class="block3sensing"}, dann `füge 1 zur Punktzahl hinzu`{:class="block3variables"}.

--- /hint ---

--- hint ---

Hier sind die neuen Code-Blöcke, die du zu deinem `wenn ich als Klon entstehe`-Skript, hinzu fügen musst:

```blocks3
change [Punkte v] by (1)

if <> then
end

<touching (Tür v)?>

set [Punkte v] to (0)
```

--- /hint ---

--- hint ---

So sollte dein Code aussehen:

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
+   if <touching (Tür v)?> then
        change [Punkte v] by (1)
    end
end
delete this clone

when flag clicked

+ set [Punkte v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Füge noch etwas mehr Code hinzu, sodass eine Katze ein "Miau" Klang spielt und verschwindet, wenn sie die Tür erreicht.

![Katzen Figur](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---