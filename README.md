# Astro Bot Image Docker

Le dockerfile contenant l'envrionnement necessaire pour que Astro-Bot Fonctionne correctement

### Installing

Pour build l'image :
```bash
docker build -t astro-bot-docker:latest .
```

Pour lancer l'image il faut indiquer l'emplacement où Astro-Bot se situe qui aura été pull auparavant:
```bash
docker run -d -v ~/Documents/Astro-Bot:/Astro-Bot astro-bot-docker:latest
```

## Links

Repository de Astro-Bot : https://github.com/Drake62610/Astro-Bot



