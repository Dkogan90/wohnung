# Wohnung Von-Stauffenberg-Straße 22 – Exposé

Statische Verkaufsseite für **wohnung.davidkogan.de**.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Exposé-Website |
| `aushang-a5.html` | A5-Aushang mit QR-Code (zum Drucken) |
| `assets/` | Optimierte Fotos, Grundriss, QR-Code |
| `docs/` | Energieausweis & Grundriss als PDF |

## Lokal ansehen

```bash
# im Projektordner
python3 -m http.server 8080
# dann: http://localhost:8080
# Aushang: http://localhost:8080/aushang-a5.html
```

## A5-Aushang drucken

1. `aushang-a5.html` im Browser öffnen  
2. **Drucken** (oder „Als PDF speichern“)  
3. Papierformat **A5**, Skalierung **100 % / tatsächliche Größe**  
4. Ränder **0**, Hintergrundgrafiken **an**

## Vor dem Go-Live prüfen

- [x] E-Mail: `david_kogan@hotmail.de`
- [x] Tel./WhatsApp: `+49 176 56967667`
- [x] Wohngeld: ca. 450 € / Monat
- [x] TG-Stellplatz geklärt (im Verkauf mit enthalten)

## Hosting (Coolify)

- **Live:** https://wohnung.davidkogan.de  
- **Coolify:** Projekt `davidkogan` · App `wohnung` · Build pack `dockerfile`  
- **GitHub:** https://github.com/Dkogan90/wohnung (`main`)  
- **Image:** nginx Alpine (`Dockerfile` + `nginx.conf`)

Deploy: Push auf `main` und in Coolify redeployen, oder:

```bash
curl -X GET "https://coolify.davidkogan.de/api/v1/deploy?uuid=z4vfr6fxsw320csa7nu6d76s" \
  -H "Authorization: Bearer $COOLIFY_TOKEN"
```
