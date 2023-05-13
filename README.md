<div align=center>
<h1>
metamob.api<br>
<img src=https://img.shields.io/badge/JavaScript-100%25-yellow?style=plastic>
<br>
</h1>
<sup>#Not dev</sup> <sup>#Only retrive last videos</sup> <sup>#youtube api</sup>
<br>
</div>
<br>
<h1>🌐API</h1>
<h2>🗝️Récupérer une clé</h2>
Pour créer votre clé, rendez-vous sur <a href="console.cloud.google.com/welcome">votre console google</a> et Créez un nouveau projet si ce n'est pas encore fait. Une fois votre projet créer, générez une clé en vous rendant dans <b>"API et services"</b> -> <b>"Identifiants"</b> -> <b>"Créer des identifiants"</b> -> <b>"Clé API"</b><br>
<br>
<h2>✨Installation</h2>

`npm install ytb_xs.js`
<br>
<h2>👀Utilisation</h2>
<h3>1. Commencez par instancier un nouveau client en fournissant votre clé API fournie par google :</h3>

```js
const { ytb_xs } = require("ytb_xs.js");

const client = new ytb_xs({ apiKey:"votre_clé_api" });
```

<img src="https://github.com/Ix-xs/ytb_xs.js/assets/114710533/fbd8e695-f68c-4548-a9cf-bdb5c5d122e4">

<br>
<h3>2. Assurez vous d'activer le service "YouTube Data API v3" dans votre bibliothèque de services :</h3>

<img src="https://github.com/Ix-xs/ytb_xs.js/assets/114710533/66c0a5db-f06a-47d2-9414-520cbef97f25">

<br>

<br>
<h3>3. Liste des appels possibles</h3>
<br>

Méthode | options | Description |
| --- | --- | --- |
| `GET.channelByUsername()` | `username`:string | Récupère les informations d'une chaîne utilisateur. |
| `GET.channelById()` | `id`:string | Récupère les informations d'une chaîne utilisateur. |
| `GET.lastVideoByUsername()` | `username`:string | Récupère les informations sur la dernière video de l'utilisateur. |
| `GET.lastVideoById()` | `id`:string | Récupère les informations sur la dernière video de l'utilisateur. |

<br>
<h3>3. Exemples</h3>
<br>


```js
const { ytb_xs } = require("ytb_xs.js");

const client = new ytb_xs({ apiKey:"votre_clé_api" });

client.GET.channelByUsername("GoogleDevelopers").then(console.log); // Renvoi les informations de la chaine utilisateur.

client.GET.channelById("UC_x5XG1OV2P6uZZ5FSM9Ttw").then(console.log); // Renvoi les informations de la chaine utilisateur.

client.GET.lastVideoByUsername("GoogleDevelopers").then(console.log); // Renvoi les informations sur la dernière video de l'utilisateur.

client.GET.lastVideoById("UC_x5XG1OV2P6uZZ5FSM9Ttw").then(console.log); // Renvoi les informations sur la dernière video de l'utilisateur.
```