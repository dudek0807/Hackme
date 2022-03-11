# Hackme1.0
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


