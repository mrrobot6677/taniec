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
6. Wartości licznkiów są widoczne w prawym dolnym rogu strony, po najechaniu na dany pdf. Do odczytywania tylko w wersji na komputer.
