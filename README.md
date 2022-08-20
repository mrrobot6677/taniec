1. Część informacji na stronie jest pobierana z pliku data.json.
2. H1 - główne hasło na stronie otwierającej
3. news - tablica `[]` - docelowo 4 obiektów `{}` odpowiadającym newsom na stronie. Każdy obiekt posiada: `title`, `image`, `text` i `fullText` wyświetlany po kliknięciu w "Więcej".
4. quarterly number - numer kwartalnika
5. quarterly_pdf - ścieżka do pliku pdf
6. quarterly - tablica `[]` z obiektami `{}` zawierającymi `title` i `texts`. W `texts` mamy tablicę `[]` w której umieszczamy paragrafy. Docelowo umieszczamy spis treści nowego numeru.
7. banner - ścieżka do baneru reklamowego
8. archives - numery archiwalne. Tablica `[]` obiektów `{}` - każdy reprezentuje jeden numer archiwalny. Posiada pola `number`, `image`, `pdf`, i tablicę `[]` `contents` w której mamy spis treści w takim samym formacie jak w sekcji kwartalnik.
9. patrons - tablica `[]` obiektów `{}` - każde reprezentuje jednego patrona. Posiada pola `image` i `text`.
10. dance_education - obiekt `{}` posiadający pola `text`, `title`, `pdf`, `number`.

### UWAGI OGÓLNE

1. Pola `number` nie mogą posiadać żadnych spacji
2. Wszystkie zdjęcia muszą znajdować się w folderze `images`
3. Wszystkie pdfy muszą znajdować się w folderze `pdf`
4. Format JSON w którym napisany jest plik jest bardzo wrażliwy na błędy, jeden brakujący przecinek wywala stronę - edycja czy dodawanie nowych obiektów musi być bardzo uważna.
5. Wszędzie tam, gdzie mamy tablicę `[]` w której są zawarte obiekty `{}`, możemy dodawać nowe obiekty `{}` z tymi samymi właściwościami, czyli jeśli obiekty w danej tablicy mają pola `title` i `image` to możemy dodać obiekt, który musi mieć także pola `title` i `image`.
6. Jeśli dodajesz nową grafikę, zdjęcie wrzuć je najpierw w optymalizator https://tinypng.com/ - pozwoli to zmniejszyć wagę zdjęcia. Dopiero tak zoptymalizowane zdjęcie umieszczasz w folderze `images`. Utrzymuj konwencję nazewnictwa zdjęć, w nazwie nie może być spacji, ani wielkich liter.

### LICZNIKI

Każdy licznik na stronie jest do podejrzenia pod danym linkiem:

1. Nowy numer kwartalnika: https://api.countapi.xyz/get/taniec-numerkwartalnika np. https://api.countapi.xyz/get/taniec-2.2022
2. Archiwalne numery: https://api.countapi.xyz/get/taniec-archiwum-numerkwartalnika np. https://api.countapi.xyz/get/taniec-archiwum-2.2018
3. Edukacja taneczna: https://api.countapi.xyz/get/taniec-edu-numer np. https://api.countapi.xyz/get/taniec-edu-1.2021
