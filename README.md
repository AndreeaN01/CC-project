1. Introducere

Crearea unei aplicatii web care sa utilizeze doua servicii in cloud, prin intermediul unui API REST. Pentru realizarea acestei aplicatii s-au folosit 2 API-uri publice: Google Maps (geocode – pentru preluarea hartilor) si Weather (forecast – pentru afisarea temperaturii, in diferite zone geografice). Pentru realizarea acesteia, s-au folosit urmatoarele tehnologii: HTML, CSS, JavaScript, MongoDB.

2. Descriere problema
 
Aplicatia creata are rolul de a afisa informatii despre vreme, mai exact temperatura dintr-o anumita zona geografica, in functie de locatia introdusa in zona de search, precum si probabilitatea averselor de ploaie din ziua respectiva. Inainte de a introduce locatia, aplicatia are si un mesaj intuitiv: “Use this site to get your weather!”. Dupa introducerea zonei si apasarea butonului search, se vor afisa informatiile necesare sub forma unui mesaj, cum este cel din imaginea de mai jos:

![image](https://user-images.githubusercontent.com/84004939/117771402-bb002f00-b23e-11eb-8d5e-e0df622dbe6d.png)


3. Descriere API
 
- Map - Geocoding API transforma o adresa de tip text in coordinate geografice: latitudine si longitudine, ce pot fi reprezentate ca un punct pe harta. Răspunsul API pentru o interogare de geocodificare returnează o colecție de caracteristici GeoJSON în format Mapbox Geocoding Response.
- Forecast API – acest API ofera informatii despre vremea si temperaturile curente din orice locatie. Cu ajutorul acestuia este afisata atat temperatura din zona geografica selectata, dar si probabilitatea averselor.

4. Flux de date
 
Exemple de request/response:

API-urile folosesc request-uri HTTP. In campul din pagina web corespunzator adresei este introdus textul: Bucuresti si se realizeaza requestul catre harti, ce transforma aceasta adresa in coordonate geografice (latitudine si longitudine), permitand translatarea adresei textuale intr-un punct pe harta, iar ulterior, prin intermediul API-ului forecast, se preiau informatiile despre vreme corespunzatoare zonei geografice selectate.

Metode HTTP

Pagina web foloseste 2 request-uri HTTP, unul pentru API-ul geocode si unul pentru API-ul forecast.
Pentru stilizarea paginii s-a folosit limbajul specific CSS.

Autentificare si autorizare servicii utilizate

Autentificarea requesturilor catre cele doua API-uri se face prin API key-uri, ce sunt introduse in url-ul request-ului. 



