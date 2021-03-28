Co to
---

Patrz [ten post na Reddicie](https://www.reddit.com/r/manga/comments/mcicbp/sl_how_to_host_a_series_on_imgur_with_guyamoe/)

Instrukcja jak coś dodać
---

1. Stwórz konto na Githubie
2. Poproś mnie o prawa (Triage to najwięcej co dostaniesz)
3. Stwórz pull requesta za zmianami (patrz co w zmianach)
4. Pingnij mnie o approva (JSONy są machine-friendly, nie user-friendly, więc trzeba sprawdzić czy json jest poprawny)
5. Kiedy PR zostanie zaaprowowany odświżenie strony z projektem powinno wystarczyć

Co w zmianach
---

1. Wrzuć rozdział na imgura. Uwaga reader sortuje alfanumerycznie więc mogą wychodzić kwiatki typu strony w kolejności:
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

Rozdziały sortowane są po last_updated, więc zalecam to incrementować. Inaczej mogą wyjść numery jak z sortowaniem stron.

Dodatkowe akcje w przypadku nowego projektu
---

1. Click added file on Github and click raw
2. Copy URL from browser to [git.io](https://git.io/) and generate short URL
3. Go to cubari.moe and paste short URL from 2