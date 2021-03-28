Co to
---

Patrz [ten post na Reddicie](https://www.reddit.com/r/manga/comments/mcicbp/sl_how_to_host_a_series_on_imgur_with_guyamoe/)

Instrukcja jak coś dodać
---

1. Stwórz konto na Githubie
2. Poproś mnie o prawa (Triage to najwięcej co dostaniesz)
3. Stwórz pull requesta za zmianami (patrz co w zmianach)
4. Pingnij mnie o approva
5. Kiedy PR zostanie zaaprowowany odświżenie strony z projektem powinno wystarczyć

Co w zmianach
---

1. Wrzuć rozdział na imgura. Uwaga reader sortuje alfanumerycznie więc mogą wychodzić kwiatki typu strony  kolejności:
1 10 100 11 ... 2 20 ... 3 4 5 6 7 8 9
2. Dodać nowy obiekt pod kluczem chapters, np.

```json
    "numer rozdziału": {
      "title": "",
      "volume": "1",
      "groups": {
        "KaguraScans": "/proxy/api/imgur/chapter/<id albumu z imgura>/"
      },
      "last_updated": "0"
    }
```
