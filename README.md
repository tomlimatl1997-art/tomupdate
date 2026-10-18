# tommupdate

Ponto unico de consulta de versao do aplicativo TomTV.

O aplicativo **apenas le** o arquivo `latest.json` na raiz da branch `main`
e compara `versionCode` com o do proprio APK. Nenhum token do GitHub e usado
pelo aplicativo.

Publicar uma release nova e um passo do programador, pelo script
`tools/publicar-release.ps1` que vem na source do aplicativo.

Formato do `latest.json`:

    {
      "versionCode": 143,
      "versionName": "1.5.120-local",
      "url": "https://github.com/OWNER/REPO/releases/download/v1.5.120-local/arquivo.apk",
      "sha256": "...",
      "notes": "...",
      "publishedAt": "2026-01-01T00:00:00Z"
    }