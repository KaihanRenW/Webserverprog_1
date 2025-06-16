# 🧠 Instuderingsfrågor – Lektion 1–5 (PHP, formulär, filer, sessioner)

Här är 50 instuderingsfrågor som täcker det vi har gått igenom hittills.  
De är uppdelade i tre kategorier:

- ✅ Flervalsfrågor (Multiple Choice)
- 💬 Öppna frågor
- 🧪 Kodfrågor

---

## ✅ Flervalsfrågor (Multiple Choice)

**1.** Vilken superglobal används för att ta emot data från ett formulär med metoden POST?  
a) `$_GET`  
b) `$_REQUEST`  
c) `$_POST`  
d) `$_SERVER`  
**Svar:** c

**2.** Vad gör funktionen `htmlspecialchars()` i PHP?  
a) Den lägger till HTML-taggar  
b) Den skyddar mot XSS genom att ersätta tecken  
c) Den rensar databasen  
d) Den skapar HTML  
**Svar:** b

**3.** Vilken metod används för att skriva till en fil i PHP?  
a) `readfile()`  
b) `file_get_contents()`  
c) `file_put_contents()`  
d) `open()`  
**Svar:** c

**4.** Vilket värde returnerar `$_SERVER["REQUEST_METHOD"]` vid formulärskickning?  
a) GET  
b) PUSH  
c) FORM  
d) POST  
**Svar:** d

**5.** Var sparas data i en session?  
a) I en cookie i webbläsaren  
b) I en variabel  
c) På serversidan  
d) I HTML-formuläret  
**Svar:** c

**6.** Vad gör `include "form.php"` i PHP?  
a) Den kör JavaScript  
b) Den inkluderar ett formulär  
c) Den importerar en databas  
d) Den kör CSS  
**Svar:** b

**7.** Vilken av dessa skapar ett nytt array-element i PHP?  
a) `$array + $newitem`  
b) `$array.append($newitem)`  
c) `$array[] = $newitem`  
d) `push($array, $newitem)`  
**Svar:** c

**8.** Vad är en JSON-fil främst till för?  
a) Styling  
b) Lagring av strukturerad data  
c) Att länka bilder  
d) Att skapa cookies  
**Svar:** b

**9.** Vilken funktion används för att konvertera JSON till PHP-array?  
a) `json_to_array()`  
b) `json_import()`  
c) `json_decode()`  
d) `array_decode()`  
**Svar:** c

**10.** Vad krävs för att använda `$_SESSION`?  
a) `enable_session()`  
b) `cookie_start()`  
c) `session_start()`  
d) `init_session()`  
**Svar:** c

---

## 💬 Öppna frågor

**11.** Vad är skillnaden mellan `$_GET` och `$_POST`?

**12.** Vad används `$_SERVER["REQUEST_METHOD"]` till?

**13.** Förklara varför `htmlspecialchars()` är viktigt när man sparar användardata.

**14.** Vad är syftet med att dela upp koden i `form.php`, `functions.php` och `index.php`?

**15.** Vad händer om du glömmer att skriva `session_start();` överst i filen?

**16.** Förklara skillnaden mellan en cookie och en session.

**17.** När kan det vara bättre att använda en JSON-fil istället för en textfil?

**18.** Vad menas med klient–server modellen?

**19.** Varför är det bra att använda `foreach` när man läser flera meddelanden från en JSON-fil?

**20.** Ge exempel på vad man kan dokumentera i ett README.md-dokument för ett webbprojekt.

---

## 🧪 Kodfrågor

**21.** Skriv ett enkelt HTML-formulär med `method="post"` som skickar `name` och `message`.

**22.** Skriv en PHP-funktion som tar emot två strängar och sparar dem i en textfil.

**23.** Hur skulle du läsa in en JSON-fil i PHP och visa varje `message` i en lista?

**24.** Visa hur man startar en session och sparar användarnamnet i `$_SESSION`.

**25.** Hur kontrollerar man att båda fälten i ett formulär är ifyllda innan man sparar?

**26.** Skriv ett exempel på hur man visar ett formulär endast om `$_SESSION["username"]` inte är satt.

**27.** Skapa en funktion `saveToJSON($user, $msg)` som lägger till ett nytt meddelande i `data.json`.

**28.** Skriv ett exempel på hur man gör en enkel redirect i PHP efter formulärskick.

**29.** Visa hur man loopar igenom ett array med `foreach` i PHP och skriver ut alla element.

**30.** Visa hur man rensar en session och skickar användaren till startsidan.

---

## 💬 Fler öppna frågor

**31.** Vad är skillnaden mellan `include` och `require`?

**32.** Vad gör `file_exists()` och när använder man det?

**33.** Beskriv syftet med `file_put_contents()` och vad som händer om man inte använder `FILE_APPEND`.

**34.** Vad menas med strukturerad data? Ge exempel.

**35.** Varför ska man validera att användaren fyller i alla fält?

**36.** Beskriv ett projekt där sessions, JSON och formulär används.

**37.** Hur kan man skydda en webbplats från användare som skriver in farlig kod?

**38.** Vad är en HTTP request och vad innehåller den?

**39.** Vad är `json_encode()` och vad används det till?

**40.** Hur kan du strukturera en mapp för ett enkelt webbprojekt?

---

## 🧪 Fler kodfrågor

**41.** Visa hur du visar meddelandet “Välkommen, Namn!” med data från `$_SESSION`.

**42.** Hur sparar du meddelanden i en JSON-array som också innehåller tidpunkt (`timestamp`)?

**43.** Gör ett formulär där användaren kan radera alla meddelanden från `data.json`.

**44.** Visa hur man läser JSON med `json_decode()` och kontrollerar att det är en array.

**45.** Skriv en PHP-kod som kontrollerar om filen `data.json` finns och annars skapar en tom array.
