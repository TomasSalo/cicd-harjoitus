# CI/CD-harjoitus

Harjoitus jatkuvasta integraatiosta ja julkaisusta (CI/CD). Pieni Java-ohjelma `SiteGen` generoi HTML-sivun, ja putki kääntää sen, ajaa JUnit-testit ja julkaisee sivun automaattisesti.

Harjoitus tehtiin alun perin Turun yliopiston GitLabissa kurssin pohjaprojektin päälle. Tässä versiossa putki on toteutettu kahdella tavalla:

- `.gitlab-ci.yml`: alkuperäinen GitLab CI -putki (build → test → deploy GitLab Pagesiin)
- `.github/workflows/ci.yml`: sama putki siirrettynä **GitHub Actionsiin**

## Putken vaiheet

1. **Build**: `javac SiteGen.java`
2. **Test**: JUnit 5 -testi varmistaa, että generoitu HTML on odotetun mukainen
3. **Deploy**: ohjelma ajetaan ja syntynyt `public/index.html` julkaistaan

## Ajo paikallisesti

```bash
javac SiteGen.java && java SiteGen
```

## Teknologiat

Java, JUnit 5, GitLab CI, GitHub Actions

## Tekijä

Tomas Salo
