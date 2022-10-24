# Intro til webutvikling

## Programvare

- [Node >= 14.0.0](https://nodejs.orgen/)
- NPM >= 5.6
- [NPX](https://www.npmjs.com/package/npx)
- Git
- [GitHub-bruker](http://github.com/)

<details>
<summary>👷 Installasjonshjelp</summary>

### Installasjon av Node og NPM

[Node](https://nodejs.org) er et veldig populært program som brukes for å kjøre JavaScript-applikasjoner, og NPM (Node Package Manager) er et veldig populært program for å håndtere installasjon av JavaScript-pakker og -programmer.

For installasjon av Node og NPM, anbefaler vi å bruke verktøyet [Node Version Manager](https://github.com/nvm-sh/nvm), som regel kjent som bare `nvm`. `nvm` gjør det veldig lett å veksle mellom ulike Node-versjoner, avhengig av hva et gitt prosjekt er krever.

0. Sjekk om du har `Node` og `NPM` installert ved å kjøre:

   ```bash
   node --version
   npm --version
   ```

   Dersom disse kommandoene skriver ut versjonsnummer, kan du hoppe over resten av stegene.

1. Installer `nvm` med denne magiske kommandoen 🪄
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
   ```
   Man bør alltid være litt kritisk når man får beskjed om å _"bare kjøre denne linja i terminalen"_ på nett, men her har vi altså kun trukket med kommandoen som står beskrevet i `nvm` sin dokumentasjon. [Ta gjerne en nøyere titt på den her.](https://github.com/nvm-sh/nvm#installing-and-updating)
2. Last ned og installer nyeste versjon av `node` og `npm` med:
   ```bash
   nvm install node
   ```
3. For å dobbeltsjekke at alt gikk som det skulle, kan du kjøre følgende for å sjekke den installerte versjonen:

   ```bash
   # Sjekk npm-versjon
   npm --version

   # Sjekk node-versjon
   node --version
   ```

### Installasjon av NPX

For å kunne kjøre JavaScript-kommandoer fra våre installerte pakker direkte fra terminalen, kan vi bruke et program som heter `npx` (Node Package Execute). `npx` kan enten kjøre lokalt installerte pakker sine programmer, eller laste ned pakker midlertidig og så kjøre dette 🤯
Vi skal bruke `npx` for å sette opp React-prosjektet vårt.

Installer `npx` med

```bash
npm install --global npx
```

`--global` gjør at pakken blir installert og tilgjengelig fra hvor som helst på datamaskinen din, og ikke bare i prosjektet man er inni.

</details>

## Workshop

### Outline

1. Opprett react applikasjon
2. Kjør opp applikasjonen lokalt
3. Gjør noen endringer på applikasjonen
4. Last opp prosjektet til et GitHub repository
5. Opprett et prosjekt i Vercel

### Steg 1: Opprett react applikasjonen 👶

Det finnes flere måter å komme i gang med et React-prosjekt. En enkel måte er å bruke [Create React App](https://create-react-app.dev/docs/getting-started/) som hjelper deg med å sette opp det man trenger for å komme i gang.

Naviger til stedet du vil opprette prosjektet og skriv følgende kommando i terminalen for å opprette prosjektet:

```
npx create-react-app <navn på applikasjon>
```

Dette vil installere nødvendige avhengigheter og sette opp et prosjekt for deg 📦

<details>
<summary><b>🤓 Protip</b></summary>

JavaScript er ikke kjent for å være det mest typesikre programmeringsspråket. I store prosjekter er det veldig vanlig å bruke [TypeScript](https://www.typescriptlang.org/), som er JavaScript utvidet med syntax for typer.

For å opprette et React-prosjekt med Typescript, kan du kjøre følgende kommando:

```
npx create-react-app <navn på applikasjon> --template typescript
```

---

</details>

### Steg 2: Kjør opp applikasjonen lokalt 💻

1. Naviger til prosjektet:

   ```
   cd <navn på app>
   ```

2. Start prosjektet lokalt:
   ```
   npm start
   ```
3. Gå til [http://localhost:3000](http://localhost:3000) i nettleseren for å se applikasjonen kjøre lokalt.

### Steg 3: Gjør noen endringer i App.js 📝

Bare kreativiteten setter grenser, gjør noe gøy i `App.js` som du vil at verden skal få se! ✨

<details>
<summary>Sliter du med å komme på noe å endre?</summary>

En enkel endring man kan gjøre er å endre teksten i `App.js`-fila.

```diff
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
-         Edit <code>src/App.js</code> and save to reload.
+         Hallo! 👋
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```

</details>

### Steg 4: Last opp prosjektet dit til et GitHub repo ☁

1. Opprett et GitHub-repo ved å gå til https://github.com/new, skriv inn et navn og trykk `create repository`
2. Fra roten av prosjektet ditt, kjør kommandoen
   ```
   git remote add origin <repository-url>
   ```
3. Vi kan nå legge til endringene våre ved å skrive
   ```
   git add <filnavn>
   ```
   etterfulgt av
   ```
   git commit -m "<endringsmelding>"
   ```
4. Deretter kan du pushe koden til GitHub:
   `git push -u origin master`

<details>
<summary>Ikke så komfortabel i kommandolinjen? ☝</summary>
Man kan også laste opp applikasjonsfilene til GitHub direkte i GitHub sitt grensesnitt. Gå til www.github.com/DittBrukernavn/DittRepository/upload. 
</details>

### Steg 5: Registrer bruker hos Vercel

For å gjøre applikasjonen din tilgjengelig for andre enn deg selv, må vi legge den et sted hvor flere kan nå den. Det finnes mange måter å gjøre dette på, den enkleste er kanskje å benytte seg av en skyplattform slik som vi skal gjøre i dag.

Denne gangen vil vi bruke [Vercel](https://vercel.com/signup) for hosting av applikasjonen vår.

Gå til [https://vercel.com/signup](https://vercel.com/signup) og registrer deg med GitHub-brukeren din.

(_andre gode alternativer for enkel hosting kan være Heroku, Google Firebase, og Netlify_)

### Steg 6: Opprett prosjekt i Vercel

Nå nærmer vi oss en applikasjon på nett! 🤩 Vi må bare få koblet opp GitHub-repoet til Vercel, slik at vi kan få koden vår på en web-server.

1. Gå til https://vercel.com/new
2. Velg "Continue with GitHub"
3. Velg GitHub-repoet du lagde tidligere i steg 4.
4. Under "Configure project" trykker deploy, uten å endre noen konfigurasjonsverdier.
5. 🚀🚀🚀🚀🚀🚀
