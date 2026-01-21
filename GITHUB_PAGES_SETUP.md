# GitHub Pages Setup - TikTok Developer Portal

TikTok verifierar URL:erna och GitHub Gist Raw-URL:er fungerar inte alltid. GitHub Pages är en bättre lösning.

## Snabbaste Metoden: GitHub Pages

### Steg 1: Skapa ett nytt GitHub Repository

1. Gå till [GitHub](https://github.com) och logga in
2. Klicka på "+" i övre högra hörnet > "New repository"
3. Namn: `tiktok-youtube-shorts-legal` (eller valfritt namn)
4. Välj "Public"
5. **Viktigt:** Kryssa INTE i "Initialize with README"
6. Klicka "Create repository"

### Steg 2: Ladda upp filerna

**Metod A: Via GitHub Web Interface (Enklast)**

1. I ditt nya repository, klicka "uploading an existing file"
2. Dra och släpp dessa filer från `legal/` mappen:
   - `terms-of-service.html`
   - `privacy-policy.html`
3. Klicka "Commit changes"

**Metod B: Via Git (Om du har Git installerat)**

```bash
cd d:\Cursor\program\TikTokYouTubeShort\legal
git init
git add terms-of-service.html privacy-policy.html
git commit -m "Add legal documents"
git branch -M main
git remote add origin https://github.com/DITT-ANVÄNDARNAMN/tiktok-youtube-shorts-legal.git
git push -u origin main
```

### Steg 3: Aktivera GitHub Pages

1. I ditt repository, gå till **Settings**
2. Scrolla ner till **Pages** (i vänstermenyn)
3. Under "Source", välj **"Deploy from a branch"**
4. Välj branch: **"main"**
5. Välj folder: **"/ (root)"**
6. Klicka **"Save"**

### Steg 4: Vänta på deployment

- GitHub Pages tar vanligtvis 1-2 minuter att deploya
- Du ser status i repository:et under "Actions" fliken

### Steg 5: Hämta dina URL:er

Efter deployment (1-2 minuter), dina URL:er blir:

```
https://DITT-ANVÄNDARNAMN.github.io/tiktok-youtube-shorts-legal/terms-of-service.html
https://DITT-ANVÄNDARNAMN.github.io/tiktok-youtube-shorts-legal/privacy-policy.html
```

**Ersätt `DITT-ANVÄNDARNAMN` med ditt faktiska GitHub-användarnamn!**

### Steg 6: Testa URL:erna

1. Öppna varje URL i webbläsaren
2. Du bör se HTML-sidan korrekt renderad
3. Om det fungerar, använd dessa URL:er i TikTok Developer Portal

## Alternativ: Använd samma repository som projektet

Om du redan har ett GitHub-repository för detta projekt:

1. Ladda upp `legal/` mappen till ditt befintliga repository
2. Aktivera GitHub Pages på samma sätt
3. Dina URL:er blir:
   - `https://DITT-ANVÄNDARNAMN.github.io/PROJEKT-NAMN/legal/terms-of-service.html`
   - `https://DITT-ANVÄNDARNAMN.github.io/PROJEKT-NAMN/legal/privacy-policy.html`

## Varför GitHub Pages fungerar bättre än Gist

- ✅ Riktiga webbservrar som TikTok kan verifiera
- ✅ HTTPS-certifikat (krävs av TikTok)
- ✅ Korrekt Content-Type headers
- ✅ Stabilare och mer professionellt
- ✅ Gratis och enkelt att underhålla

## Troubleshooting

**"Page not found" efter deployment?**
- Vänta 2-3 minuter extra
- Kontrollera att filerna är i root-nivån (inte i en undermapp)
- Verifiera att GitHub Pages är aktiverat i Settings

**TikTok accepterar fortfarande inte URL:erna?**
- Kontrollera att URL:erna är HTTPS (inte HTTP)
- Öppna URL:erna i en inkognito-fönster för att testa
- Se till att sidorna laddas korrekt med HTML-innehåll
