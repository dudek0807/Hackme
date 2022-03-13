# Hackme 1.0
## Pierwsze zadanie
![image](https://user-images.githubusercontent.com/73962599/157893427-53f3cb15-594c-483e-8dc7-49bb1d2223cc.png)

(Każde kolejne zadanie wygląda w podobny sposób, więc kolejne screen'y będą jedynie z kodu źródłowego strony)

W widoku pierwszego zadania nie dzieje się za dużo. Dlatego pierwszym krokiem jest zbadanie kodu źródłowego strony za pomocą kombinacji klawiszy `Ctrl + U`

![image](https://user-images.githubusercontent.com/73962599/157895459-f228d8b6-3ee6-4bcd-a7c9-a5d1ec3a93a5.png)

Z kodu javascript, z funkcji `sprwdz()` można znaleźc hasło, które brzmi `'a jednak umiem czytac'`. Wpisując je przenosi nas do zadania drugiego. Przejść do zadania drugiego można również w inny sposób. Fragment kodu tej funkcji `self.location.href='ok_next.htm';` jasno pokazuje, że następne zadanie znajduje się pod adresem `ok_next.htm`, wystarczy podmienić `level1.htm` na `ok_next.htm` w pasku adresu przeglądarki.

## Drugie zadanie
![image](https://user-images.githubusercontent.com/73962599/157895932-f55eaf4b-6cb6-446a-a4cb-67a2a160f118.png)

Z kodu źródłowego drugiego zadania mżna zauważyć, że hasło znajduje się w zmiennej `has`, w celu znalezienia tego hasła otworzono zewnętrzny plik javascript `haselko.js`

![image](https://user-images.githubusercontent.com/73962599/157896242-7392534d-2142-4546-bfc6-712ba37afcf2.png)

Z tego pliku dowiadujemy się, że hasło brzmi `to bylo za proste`. Poznajemy też adres do następnego zadania. By do niego przejść trzeba podać hasło, albo podmienić adres, podobnie jak to można było zrobić w zadaniu pierwszym.

## Trzecie zadanie
![image](https://user-images.githubusercontent.com/73962599/157897080-f3682677-b175-4798-8436-dd63960f99c5.png)

Analizując kod źródłowy można zauważyć, że korzystając z przeglądarki `Netscape Navigator` lub `Microsoft Internet Explorer` nie będzie mozna skorzystać z prawego przycisku myszy by wybrać opcję `Źródło strony`. Z racji, że od początku używany jest skrót klawiszowy `Ctrl + U` (oraz przeglądarka `Opera GX`) ten problem tu nie dotyczy.

Analizując kod dalej widzimy, że hasło znajduje się w zmiennej `ost`, tak samo jak dalszy adres, więc nie będzie mozna skorzystać ze sztuczki ominięcia wpisywania hasła. Na szczęście widać jak wartość zmiennej ost powstaje: `ost=literki.substring(2,4)+'qwe'+dod.substring(3,6);`. zmienne `literki` oraz `dod` są podane: 
`var literki='abcdefgh';`
`var dod='unknow';`
Funkcja `substring(a, b)` zwraca fragment tekstu (podciąg znaków) od wskazanej pozycji początkowej `a` (licząd od zera) do pozycji końcowej `b` (opcjonalnej, nie wliczając tej pozycji). Znając definicję tej funkcji, zmienną ost mozna zapisać jako `ost='cd'+'qwe'+'now'`. Czyli hasło to `cdqwenow`.

## Czwarte zadanie
![image](https://user-images.githubusercontent.com/73962599/157900883-3a23040b-22bc-48aa-acd1-4ce9c43f0f08.png)

Z kodu tego zadania widać, że hasło to wynik zadania matematycznego `(Math.round(6%2)*(258456/2))+(300/4)*2/3+121`. Po kolei: `(Math.round(6%2)*(258456/2)` jest równy 0. `6%2` to operacja modulo, czyli zwraca resztę z dzielenia. 6 dzielone na 2 ma resztę 0, więc `0*(258456/20=0`. Dodajemy do tego `(300/4)*2/3+121` co daje `171` i takie jest też hasło.

## Piąte zadanie
![image](https://user-images.githubusercontent.com/73962599/157902353-ff568fa6-d3a7-4695-a7ce-20813cfff7d1.png)

Wartość widoczna na ekranie zwiększa się co sekundę.

![image](https://user-images.githubusercontent.com/73962599/157902557-055c5840-e7ac-4c86-b476-cc3c23051e40.png)

W funkcji `sprawdz()` widać, że warunkiem przejścia do nastepnego zadania jest `ile==861`, jednak 861 nie jest naszym hasłem. By wykalkulować wartość zmiennej ile trzeba skorzystać z równania `ile=((seconds*(seconds-1))/2)*(document.getElementById('pomoc').value%2);`. `document.getElementById('pomoc').value` jest wartością, którą wpisujemy, jest naszym hasłem. `seconds` to wartość, która na głównej zwiększa się o jeden co sekundę, jest to po prostu "minutnik", który ponowne odliczanie zaczyna po właśnie minucie. Znając wymaganą wartość `ile` można obliczyć ile muszą wynosić wartości `seconds` oraz nasze hasło. Wartość, którą musimy wpisać do `Cyfry pomocniczej` musi być nieparzysta, ponieważ `(seconds*(seconds-1)/2)` jest mnożona przez resztę z dzielenia naszego hasła przez 2. Przyjmując `x=seconds` możemy zapisać równanie jako:
<sup>1</sup>&frasl;<sub>2</sub>(x<sup>2</sup> - x) = 861 => x<sup>2</sup> - x = 1722 => x<sup>2</sup> - x - 1722 = 0 => (x - 42)(x + 41) = 0
Z równania wyszło, że x = 42 lub x = -41, z racji tego, że sekundy nie mogą być ujemne, jako hasło należy wpisać dowolną dodatnią nieparzystą liczbę w momencie kiedy licznik wyświetla `42`

## Szóste zadanie
![image](https://user-images.githubusercontent.com/73962599/157912239-8f38ded8-aea5-4607-a15b-edba119e3978.png)

Zmienna `zaq` to nasze hasło. Jezeli jest równa zmiennej hsx, przechodzimy dalej. Podane są wartości zmiennych `hsx`, `licznik` oraz `znak`, które są modyfikowany w pętli oraz `lit='abcdqepolsrc'`, z której wyciągany jest podciąg dodawany do zmiennej hsx. W pierwszym przejściu pętli `i` jest równe 1, więc `lit.substring(i,i+1)` ma wartość `b`, oraz `licznik` zwiększa wartość do 1, więc znak z funkcji warunkowej if przybiera wartość `x`. Do zmiennej hsx dodawany jest ciąg znaków `bx`. W drugim przejściu pętli `i` jest równe 3, więc podciąg wyciągnięty z `lit` ma wartość `d`, oraz `licznik` zwiększa wartość do 2, więc `znak` przybiera wartość `_`. Do hsx dodwany jest ciąg znaków `d_`, więc `hsx=bxd_`. W trzecim przejściu pętli `i` jest równe 5, więc wyciągany podciąg ma wartość `e`, oraz `licznik` zwiększa się do 3, więc `znak` przybiera wartość `x`. Do hsx dodawany jest string `ex`. W tym momencie hsx ma wartość `bxd_ex`. Na samym końcu do hsx dodawany jest wyciągnięty z niego substring `_ex` (`hsx.length=6`, więc `hsx.substring(3, 6) = _ex`). Nasze haslo, które jest jednocześnie hsx ma wartość `bxd_ex_ex`.

## Siódme zadanie
![image](https://user-images.githubusercontent.com/73962599/157915466-c468625b-da4f-4c67-b9c6-b093c4a6f37b.png)

Z kodu można zauważyć, że hasło to zmienna `wyn`, która jest tworzona dodając kolejne wartości `ly`, których wartość jest określana na podstawie wartości kolejnych znaków hasła (`lx`). Wiedząc, że zmienna `wyn` musi miec wartość `plxszn_xrv` można "odszyfrować" hasło. Jeżeli `ly=p` to `lx=k` i tak dalej. Hasło ostatecznie to `kocham cie`.

## Ósme zadanie
![image](https://user-images.githubusercontent.com/73962599/157921321-50e2aac6-0c48-4686-82d4-30f09943814c.png)

Z fragmentu kodu `document.write('<\s'+'c'+'r'+'i'+'p'+'t src="%7A%73%65%64%63%78%2E%6A%73"><\/s'+'c'+'r'+'i'+'p'+'t'+'>');` możemy wyróżnić zaszyfrowany tekst `%7A%73%65%64%63%78%2E%6A%73`, który prawdopodobnie jest ścieżką do pliku javascript'u. Potwierdza to nam inny fragment `<script src="%70%61%73%73%77%64.js"></script>`, który po kliknięciu przenosi nas do pliku passwd.js

![image](https://user-images.githubusercontent.com/73962599/157921695-284bcc32-ada3-44bd-8ae7-02ebefbda818.png)

![image](https://user-images.githubusercontent.com/73962599/157921728-ab81a4cf-bf3d-405f-b27d-1dcc9bf0abf0.png)

`passwd.js` zostało zakodowane za pomocą `urlencode`, więc by odczytać wartość drugiego dołączonego pliku javascript zastosowano `urldecode`. Plik nosi nazwę `zsedcx.js`. Zawartość tego pliku to:

![image](https://user-images.githubusercontent.com/73962599/157922419-6bcde103-788c-430b-8636-324c676263a3.png)

Są to cztery zmienne `ax`, `bx`, `cx` oraz `get`, których wartości (jak łatwo policzyć) to kolejno, 6, 3, 9, 0.
W kolejnych krokach zostaną podane wartości zmienione w danym przejściu pętli:

* i=0, qet=0, qet+i=0, get=10, wyn=q
* i=2, qet=1, qet+i=3, get=20, wyn=qr
* i=4, qet=2, qet+i=6, get=30, wyn=qru
* i=6, qet=3, qet+i=9, get=40, wyn=qrup
* i=8, qet=4, qet+i=12, get=50, wyn=qrupj
* i=10, qet=5, qet+i=15, get=60, wyn=qrupjf

Po ostatnim przejściu pętli do zmiennej `wyn` dodany jest wynik mnożenia zmiennych odczytanych z pliku, więc `wyn=qrupjf162` i to jest nasze hasło. Co ciekawe zmienna get była zwiększana, jednak nie była wykorzystana do modyfikowania wartości zmiennej wyn.

![image](https://user-images.githubusercontent.com/73962599/157925495-f7c5fb09-0865-4cc4-b486-45e8ef113f2f.png)

# Hackme 2.0
## Pierwsze zadanie

![image](https://user-images.githubusercontent.com/73962599/158023669-f29a70a0-4ef4-4f05-a102-eeafa67c38c6.png)

Po kodzie źródłowym jaso widać, że hasło to wartość bloku `formularz` (`if (document.getElementById('formularz').value==document.getElementById('haslo').value)`), czyli `text`.

## Drugie zadanie

![image](https://user-images.githubusercontent.com/73962599/158028951-28a9a0cf-76d8-43e3-a8a2-c43c462ef70c.png)

W tym zadaniu hasło to wartość `unescape('%62%61%6E%61%6C%6E%65')`, czyli czas wykonać urldecode. Po dekodowaniu wychodzi, że hasło to `'banalne`.

## Trzecie zadanie

![image](https://user-images.githubusercontent.com/73962599/158029037-021f9885-b41e-4bce-a936-0841682126fe.png)

By zdobyć hasło do trzeciego zadnia, trzeba zamienić widoczną wartośc binarną na decymalną. Czyli 10011010010<sub>2</sub> = 1234<sub>10</sub>

## Czwarte zadanie

![image](https://user-images.githubusercontent.com/73962599/158029179-0686a5d7-d5ff-44ec-8ae6-081a3569abe4.png)

![image](https://user-images.githubusercontent.com/73962599/158029185-91ead903-c753-4462-aa52-21251be8e581.png)

To zadanie jest inne niż wszystkie pozostałe. By znaleźć cokolwiek ciekawego należy wyłączyć działanie skryptów javascript dla tej strony.

![image](https://user-images.githubusercontent.com/73962599/158029229-1e62b4d7-c438-4b08-8f07-2c1e997f27db.png)

Po wyłączeniu, strona wygląda następująco:

![image](https://user-images.githubusercontent.com/73962599/158029274-9395eeba-ed76-4cdc-a164-7428901faf76.png)

Jednakże po kliknięciu w link zostajemy przekierowani na stronę twórcy gry.

![image](https://user-images.githubusercontent.com/73962599/158029307-66fc4572-a73f-442a-924e-2522ca780a71.png)

Badając element znajdujemy skrypt, który pozwoli nam przejść dalej. 

![image](https://user-images.githubusercontent.com/73962599/158029342-c087da73-fd67-426f-8e59-21467bf791d4.png)

Patrząc na parametr `cos` od razu na myśl przychodzi użycie urldecode, wartośc to `258`. Wartość hasła musi wynosić `cos.toString(16)`, czyli 258 trzeba zamienić na jej odpowiednik w systemie szesnastkowym. Hasło to `102`. Do następnego poziomu można przejść na dwa sposoby. Podmieniając aktualny `1234.htm` na `102.php`, lub włączyć spowrotem działanie skryptów javascript i wpisać hasło.

## Piąte zadanie

![image](https://user-images.githubusercontent.com/73962599/158029593-d0eaa5c8-df25-4ba3-912b-b8683d0b8429.png)

W tym zadaniu używany jest skrypt php, więc nie podejrzymy jego dokładnej zawartości. Podane jest źródło skryptu, jednak nie poznamy z niego loginu i hasła. Po podaniu poprawnego loginu, flaga `$log` ustawiana jest na 1, tak zamo jest w przypadku flagi `$has`.
Po wpisaniu do pola login `login` i do pola hasło `haslo` warto zwrócić uwagę na zmiany w adresie strony.

![image](https://user-images.githubusercontent.com/73962599/158029763-b320eadf-aba3-4b8f-9d39-ae4047e8c8a8.png)

Skoro tu widnieją zmienne `login` orazz `haslo`, możliwe jest też zmodyfikowanie naszych flag modyfikując adres na `https://uw-team.org/hm2/102.php?log=1&has=1`

![image](https://user-images.githubusercontent.com/73962599/158029819-ab768160-5175-4d6e-8d75-3cfbcb8165fc.png)

## Szóste zadanie

![image](https://user-images.githubusercontent.com/73962599/158029839-53bbf673-c299-476f-847a-9ae7aa5f12a0.png)

W tym momencie należy odczytać zawartość `cookie`, które zostało przysłane.

![image](https://user-images.githubusercontent.com/73962599/158029871-ed8b007b-c9c6-45f7-99ce-44d7e08148d9.png)

Jak widać nasze ciasteczko z wróżbą nazywa się `nastepna_strona`, a wróżba to `ciastka.htm`. Podmieniamy `url.php` na `ciastka.htm` i przechodzimy do zadania siódmego.

## Siódme zadanie

![image](https://user-images.githubusercontent.com/73962599/158030242-00b11ad8-10d5-4523-b0b9-80b8eb5f04f0.png)

![image](https://user-images.githubusercontent.com/73962599/158030276-f5549ad6-55d2-48e5-8705-5b342d69ce4a.png)

W tym zadaniu podając złe hasło zostajemy przekierowani na stronę `zle.htm`, zobaczmy jaki jest jej kod:

![image](https://user-images.githubusercontent.com/73962599/158030318-32b17f35-c4b7-4510-a8bf-61b351320a27.png)

W kodzie strony `ciastka.htm` widzimy ciekawy fragment: `src="include/'+haslo+'.js"`. Zobaczny więc zo znajduje się w katalogu include. By do nie go wjeść musimy w adres strony wpisać `https://uw-team.org/hm2/include`

![image](https://user-images.githubusercontent.com/73962599/158030616-d5a760fe-502f-4786-a61d-75a9b59c443a.png)

Zawartość `cosik.js` to `strona='listing.php';` więc by przejść na tą stronę podmieniamy ją w adresie lub podajemy w haśle `cosik`.

## Ósme zadanie

![image](https://user-images.githubusercontent.com/73962599/158030763-2e3eab93-a793-4406-a76e-e87d58a5c289.png)

W tym zadaniu można wyłączyć skrypt php tak jak w jendym z poprzednich zadań, lub podmienić na stronie `onet.pl` jeden z linków referencyjnycj na `uw-team.org/hm2/listing.php`. W moim przypadku wykonam tą drugą opcję.

![image](https://user-images.githubusercontent.com/73962599/158030866-dd604b6b-3237-4ee6-a089-a2d2b5d61374.png)

Wykorzystam odnośnik do podstrony onetu `sympatia.onet.pl`. Klikam w odnośnik prawym przyciskiem myszy i klikam `Zbadaj element`. Następnie podmieniam link referencyjny na `http://http://uw-team.org/hm2/listing.php` i przechodzę na stronę.

![image](https://user-images.githubusercontent.com/73962599/158030976-0f26175e-bad2-45ad-8654-71a03602831b.png)

![image](https://user-images.githubusercontent.com/73962599/158031005-15d27179-223c-4789-abcd-c46ef9c42c64.png)

![image](https://user-images.githubusercontent.com/73962599/158031018-bd010a0a-2288-4d9f-bdd6-070ea00089a0.png)

W kodzię źródłowym widać ukryty div o id `ukryte`, więc usuńmy `display:hidden`. Czcionka ustawiona jest na czarną, więc trzeba będzie zaznaczyć tekst by go odczytać.

![image](https://user-images.githubusercontent.com/73962599/158057488-b581c175-e2c2-4da1-b2ca-226bb76bfaf2.png)

Po wpisaniu hasła wyświetla się informacja, że następny etap jest ukryty w pliku `pokaz.php`. Przechodzimy do niego podmieniając go w pasku adresu.

## Dziewiąte zadanie

![image](https://user-images.githubusercontent.com/73962599/158057613-72445b49-c97f-4c0f-a42c-9c2b9715df21.png)

Dostęp do strony jest po godzinie 1 w nocy. Patrząc w kod źródłowy możena to obejść lub wyłączając działanie javascriptu.

![image](https://user-images.githubusercontent.com/73962599/158057649-f43e09d8-c7f5-4b3b-9537-837f70107894.png)

![image](https://user-images.githubusercontent.com/73962599/158057678-37f77a71-f2d5-4ccf-a678-fddf5b96e0e0.png)

Kopiując liczby binarne i zamieniając je na ASCII dostaniemy wiadomość `gratulacje! udało Ci się ukończyć te wersje Hackme.`

![image](https://user-images.githubusercontent.com/73962599/158057723-453138c0-0839-401f-b187-749c12d4d4ce.png)













