# 📝 Inlämningsuppgift – Vecka 1: Grundläggande PHP + Superglobals

## 🎯 Uppgift: Skapa en interaktiv hälsningssida med felsökning

Du ska skapa en dynamisk PHP-webbsida som:

1. Tar emot användarens **namn** och **favoritdjur** via ett formulär
2. Identifierar om formuläret skickades med **POST** eller **GET**
3. Visar ett personligt meddelande till användaren
4. Skriver ut superglobalerna `$_POST`, `$_GET`, `$_REQUEST`, och `$_SERVER` i ett `<pre>`-block för felsökning
5. Använder funktionen `htmlspecialchars()` för att skydda användarinmatning

---

## 🧱 Strukturkrav

- Formulär med minst två fält:
  - `name` (namn)
  - `animal` (favoritdjur)
- Använd `method="post"` i formuläret
- Använd `$_SERVER['REQUEST_METHOD']` för att kontrollera vilken metod som använts
- Visa ett personligt meddelande på sidan
- Skriv ut alla superglobaler med `print_r()` inuti ett `<pre>`-block

---

## 🧪 Exempel på utskrift

```text
Hej Alice! En katt är ett fantastiskt djur!
```

I `<pre>`-blocket:

```
==== POST ====
Array
(
    [name] => Alice
    [animal] => katt
)

==== SERVER ====
Array
(
    [REQUEST_METHOD] => POST
    [SCRIPT_NAME] => /greeting.php
    ...
)
```

---

## 📂 Filnamn och upplägg

- Filnamn: `greeting.php`
- Både HTML och PHP ska ligga i samma fil
- Koden ska vara kommenterad så att varje del är lätt att förstå

---

## 🌟 Bonus (valfritt för extra poäng)
- Lägg till en version med `method="get"` och hantera båda metoderna i samma fil
- Lägg till ett tredje fält, t.ex. favoritfärg
- Spara användarens favoritdjur i en `$_SESSION`-variabel

