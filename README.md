# intro-til-webutvikling-2022
Workshop med Navet oktober 2022. 

## Programvare

* [Node >= 14.0.0](https://nodejs.orgen/)
* npm >= 5.6
* Git
* [GitHub bruker](http://github.com/)


## Workshop

### Outline
1. Opprett react applikasjon
2. Kjør opp applikasjonen lokalt
3. Gjør noen endringer på applikasjonen
4. Last opp prosjektet til et GitHub repository
5. Opprett et prosjekt i Vercel

### Steg 1: Opprett react applikasjonen 👶
Det finnes flere måter å komme i gang med et react prosjekt. En enkel måte er å bruke [Create React App](https://create-react-app.dev/docs/getting-started/) som hjelper deg med å sette opp det man trenger for å komme i gang.


Naviger til stedet du vil opprette prosjektet og skriv følgende kommando i terminalen for å opprette prosjektet: 

```npx create-react-app <navn på applikasjon>``` 

Dette vil installere nødvendige avhengigheter og sette opp et prosjekt for deg 📦

### Steg 2: Kjør opp applikasjonen lokalt 💻

`cd <navn på app>`

`npm start`

Gå til `http://localhost:3000/` i nettleseren for å se applikasjonen kjøre lokalt. 


### Steg 3: Gjør noen endringer i App.js 📝
Bare kreativiteten setter grenser, gjør noe gøy i `App.js` som du vil at verden skal få se! 

### Steg 4: Last opp prosjektet dit til et GitHub repo ☁

1. Opprett et GitHub-repo ved å gå til https://github.com/new, skriv inn et navn og trykk `create repository`
2. Fra roten av prosjektet ditt, kjør kommandoen `git remote add origin <repository-url>`
3. Deretter kan du pushe koden til GitHub: 
`git push -u origin master` 

<details>
<summary>Ikke så komfortabel i kommandolinjen? ☝</summary>
Man kan også laste opp applikasjonsfilene til GitHub direkte i GitHub sitt grensesnitt. Gå til www.github.com/DittBrukernavn/DittRepository/upload. 
</details>


### Steg 5: Registrer bruker hos Vercel 
For å gjøre applikasjonen din tilgjengelig for andre enn deg selv, må vi legge den et sted hvor flere kan nå den. Det finnes mange måter å gjøre dette på, den enkleste er kanskje å benytte seg av en skyplattform slik som vi skal gjøre i dag.

Denne gangen vil vi bruke [Vercel](https://vercel.com/signup) for hosting av applikasjonen vår. 

Gå til https://vercel.com/signup og registrer deg med GitHub-brukeren din.


(_andre gode alternativer for hosting kan være Heroku, Google Firebase, og Netlify_)

### Steg 6: Opprett prosjekt i Vercel
Nå nærmer vi oss en applikasjon på nett! 🤩 Vi må bare få koblet opp GitHub-repoet til Vercel, slik at vi kan få koden vår på en web-server. 

1. Gå til https://vercel.com/new
2. Velg "Continue with GitHub"
3. Velg GitHub-repoet du lagde tidligere i steg 4.
4. Under "Configure project" trykker deploy, uten å endre noen konfigurasjonsverdier.
5. 🚀🚀🚀🚀🚀🚀 
