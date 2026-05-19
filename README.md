[README.md](https://github.com/user-attachments/files/28026258/README.md)
# DocScan

Interní Streamlit aplikace pro zpracování provozních dokumentů, výdej MČDP/OOPP a kontrolu evidence.

## Co aplikace řeší

- evidence a analýza faktur za energie
- výdej MČDP po kvartálech
- evidence OOPP pomůcek
- tisk předávacích protokolů MČDP a OOPP
- kontrola podpisů a převzetí přes QR / 2FA stránku
- dashboard OOPP & MČDP nad daty z Google Sheets

## Moduly

### Energie

Slouží pro nahrání dokumentů, analýzu faktur, zobrazení výsledků a export dat.

### OOPP & MČDP

Obsahuje:

- Dashboard
- Výdej MČDP
- Evidence OOPP
- Tisk protokolu MČDP
- Tisk protokolu OOPP

Dashboard načítá data z Google Sheets:

- `MCDP_CZLC4`
- `OOPP_CZLC4`
- `Podpisy`
- `Přehled`

### Faktury

Modul je připravený jako další krok.

### Smlouvy

Modul je připravený jako další krok.

## Google Sheets

Aplikace komunikuje s Google Sheets přes Google Apps Script endpoint uložený v `app.py`.

Používané listy:

- `MCDP_CZLC4`
- `OOPP_CZLC4`
- `Podpisy`
- `Přehled`

## Spuštění lokálně

1. Nainstalovat závislosti:

```bash
pip install -r requirements.txt
```

2. Spustit aplikaci:

```bash
streamlit run app.py
```

3. Otevřít v prohlížeči:

```text
http://localhost:8501
```

## Soubory

- `app.py` hlavní Streamlit aplikace
- `podpis_2fa.html` stránka pro potvrzení převzetí / podpis
- `requirements.txt` seznam knihoven

## Stav

Hotové:

- základní vzhled aplikace
- energie
- MČDP výdej
- OOPP evidence
- PDF protokoly
- OOPP & MČDP dashboard

Rozpracované:

- Faktury
- Smlouvy

