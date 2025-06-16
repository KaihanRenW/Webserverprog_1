# 🧠 Facit – Instuderingsfrågor Lektion 1–5

## ✅ Flervalsfrågor – Svar

1. c  
2. b  
3. c  
4. d  
5. c  
6. b  
7. c  
8. b  
9. c  
10. c

---

## 💬 Öppna frågor – Förslag på svar

11. `$_GET` skickar data via URL:en, `$_POST` skickar det i kropp (body) av request. POST används för känsligare data.  
12. För att kontrollera om ett formulär har skickats och vilken metod som används (GET eller POST).  
13. Förhindrar att användaren skriver in skadlig HTML eller JavaScript. Skyddar mot XSS-attacker.  
14. Det gör koden mer läsbar och organiserad. Varje fil har ett tydligt ansvar.  
15. `$_SESSION` fungerar inte utan `session_start()` – ingen data kan sparas eller läsas.  
16. Cookie sparas i webbläsaren. Session sparas på servern. Session är säkrare.  
17. När man vill spara flera värden strukturerat som array eller objekt.  
18. Klient–server modellen innebär att webbläsaren (klienten) skickar förfrågningar till servern som behandlar dem och skickar tillbaka svar.  
19. För att skriva ut flera meddelanden utan att behöva använda index manuellt.  
20. Beskrivning av projektet, hur det fungerar, vilka filer som finns och hur man kör det.

---

## 🧪 Kodfrågor – Exempelsvar

21.  
```html
<form method="post">
  <input name="name">
  <textarea name="message"></textarea>
  <button type="submit">Skicka</button>
</form>
```

22.  
```php
function saveToFile($name, $message) {
  $line = $name . ": " . $message . "\n";
  file_put_contents("data.txt", $line, FILE_APPEND);
}
```

23.  
```php
$data = json_decode(file_get_contents("data.json"), true);
foreach ($data as $entry) {
  echo "<p>" . $entry["message"] . "</p>";
}
```

24.  
```php
session_start();
$_SESSION["username"] = "Ren";
```

25.  
```php
if (!empty($_POST["name"]) && !empty($_POST["message"])) {
  // spara
}
```

26.  
```php
if (!isset($_SESSION["username"])) {
  include "form.php";
}
```

27.  
```php
function saveToJSON($user, $msg) {
  $data = [];
  if (file_exists("data.json")) {
    $data = json_decode(file_get_contents("data.json"), true);
  }
  $data[] = ["username" => $user, "message" => $msg];
  file_put_contents("data.json", json_encode($data, JSON_PRETTY_PRINT));
}
```

28.  
```php
header("Location: index.php");
exit();
```

29.  
```php
foreach ($array as $item) {
  echo $item;
}
```

30.  
```php
session_start();
session_destroy();
header("Location: index.php");
exit();
```

---

## 💬 Fler öppna frågor – Förslag på svar

31. `include` ger en varning om filen saknas. `require` stoppar hela programmet om filen saknas.  
32. Kontrollerar om en fil finns. Används för att undvika fel när man ska läsa in en fil.  
33. `file_put_contents()` skriver till en fil. Utan `FILE_APPEND` skriver den över allt som fanns innan.  
34. Data som är ordnad, t.ex. som array eller objekt. JSON är ett exempel.  
35. För att undvika tomma inlägg och förbättra användarupplevelse.  
36. Gästbok, kommentarsfält, enkla bloggverktyg.  
37. Använd `htmlspecialchars`, validera input, undvik eval() och exekvering av data.  
38. En HTTP request innehåller metod (GET/POST), headers, body och URL.  
39. `json_encode()` gör om array till JSON-sträng. Används för att spara i JSON-fil.  
40. Separera `index.php`, `form.php`, `functions.php`, `data.json` i mappar för struktur.

---

## 🧪 Fler kodfrågor – Exempelsvar

41.  
```php
echo "Välkommen, " . $_SESSION["username"];
```

42.  
```php
$data[] = [
  "username" => $user,
  "message" => $msg,
  "timestamp" => date("Y-m-d H:i:s")
];
```

43.  
```php
<form method="post">
  <button name="clear" type="submit">Radera allt</button>
</form>

<?php
if (isset($_POST["clear"])) {
  file_put_contents("data.json", json_encode([]));
}
```

44.  
```php
$data = json_decode(file_get_contents("data.json"), true);
if (is_array($data)) {
  // ok
}
```

45.  
```php
if (!file_exists("data.json")) {
  $data = [];
} else {
  $data = json_decode(file_get_contents("data.json"), true);
}
```