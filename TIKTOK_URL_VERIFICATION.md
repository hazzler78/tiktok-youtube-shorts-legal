# TikTok URL Verification Guide

TikTok kräver att du verifierar dina Terms of Service och Privacy Policy URL:er genom "URL properties" i Developer Portal.

## Steg-för-steg Verifiering

### Steg 1: Gå till URL Properties i TikTok Developer Portal

1. Logga in på [TikTok Developer Portal](https://developers.tiktok.com/)
2. Gå till din app
3. Navigera till **"URL properties"** eller **"App Settings"**
4. Hitta sektionen för **"Terms of Service URL"** och **"Privacy Policy URL"**

### Steg 2: Välj Verifieringsmetod

TikTok erbjuder två metoder:

#### Metod A: By URL Prefix (Rekommenderat för GitHub Pages)

1. Klicka på **"Verify properties"** eller **"Verify URL"**
2. Välj **"By URL prefix"**
3. Ange din fullständiga URL:
   - Terms: `https://hazzler78.github.io/tiktok-youtube-shorts-legal/terms-of-service.html`
   - Privacy: `https://hazzler78.github.io/tiktok-youtube-shorts-legal/privacy-policy.html`
4. TikTok kommer att generera en **verifieringsfil** (t.ex. `tiktok-verification.txt` eller liknande)
5. **Ladda ner** denna fil

#### Metod B: By Domain (Alternativ)

1. Välj **"By Domain"**
2. Ange domänen: `hazzler78.github.io`
3. Följ TikTok's DNS-verifieringsinstruktioner

### Steg 3: Ladda upp Verifieringsfilen till GitHub Pages

**Om du valde Metod A (By URL prefix):**

1. Ladda ner verifieringsfilen från TikTok
2. Ladda upp den till ditt GitHub repository:
   ```bash
   cd d:\Cursor\program\TikTokYouTubeShort\legal
   # Kopiera verifieringsfilen hit
   git add tiktok-verification.txt  # eller vad filen heter
   git commit -m "Add TikTok verification file"
   git push
   ```
   
   **ELLER** via GitHub web interface:
   - Gå till ditt repository
   - Klicka "Add file" > "Upload files"
   - Ladda upp verifieringsfilen
   - Commit

3. Verifieringsfilen måste vara tillgänglig på:
   - `https://hazzler78.github.io/tiktok-youtube-shorts-legal/tiktok-verification.txt`
   - (eller vad TikTok specificerar)

### Steg 4: Slutför Verifieringen

1. Gå tillbaka till TikTok Developer Portal
2. Klicka på **"Verify"** eller **"Complete verification"**
3. TikTok kommer att kontrollera att verifieringsfilen finns på rätt plats
4. Om allt är korrekt, kommer URL:erna att markeras som verifierade ✅

## Viktiga Punkter

- ⚠️ **Verifieringsfilen måste vara publikt tillgänglig** på exakt den URL TikTok specificerar
- ⚠️ **GitHub Pages kan ta 1-2 minuter** att deploya nya filer
- ⚠️ **Kontrollera stavningen** av filnamnet - det måste matcha exakt
- ⚠️ **Filen måste vara i root** av GitHub Pages-siten (inte i en undermapp om TikTok inte specificerar det)

## Troubleshooting

**"Verification failed" eller "File not found"?**
- Vänta 2-3 minuter efter att du laddat upp filen
- Kontrollera att filnamnet matchar exakt vad TikTok specificerar
- Öppna verifieringsfilens URL direkt i webbläsaren för att verifiera att den är tillgänglig
- Kontrollera att GitHub Pages är aktiverat och deployat

**"URL not accessible"?**
- Kontrollera att GitHub Pages är aktiverat i repository Settings
- Verifiera att URL:erna fungerar när du öppnar dem i webbläsaren
- Se till att filerna är i rätt branch (main/master)

## Efter Verifiering

När URL:erna är verifierade:
- ✅ Du kan fortsätta med app-registreringen
- ✅ Du kan aktivera Content Posting API
- ✅ Du kan gå vidare med OAuth-setup
