---
transition: fade-out
---

# Introduction

Avant OpenAPI, il y avait Swagger.

## 2011

- Créateur: **Tony Tam**, co-fondateur de Wordnik.
- Source majeure de frustration: **manque d'automatisation**
     - Documentation d'API
     - Génération de *client SDK*
- Il commence à travailler sur une structure de données permettant de décrire les **API HTTP**.
<br>
<br>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
level: 2
---

# Swagger

## Quelques dates

|                                                    |  |                             |
| ---------------------------------------------------| --- | --------------------------- |
| 1.0              | 2011-08-11     | Première version de la spécification Swagger |
| 1.1              | 2012-08-22     | Swagger 1.1 |
| 1.2              | 2014-09-08     | Première release formelle |
| 2.0 | 2014-09-08    | Swagger 2.0 |
| Acquisition par *SmartBear Software* | 2015-03     | SmartBear acquiert Swagger |
| Initiative OpenAPI (OAI) | 2015-11     | SmartBear fait le don de la spécification à l'initiative OpenAPI |

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: slide-up
level: 2
---

# OpenAPI

|                                                    |  |                             |
| ---------------------------------------------------| --- | --------------------------- |
| 3.0             | 2017-07-26   | Spécification OpenAPI 3.0 (OAS) |
| ...             |     | |
| 3.1.0             | 2021-02-15    | Spécification OpenAPI 3.1.0 |
| ...             |     | |
| 3.2.0             | 2025-09-19     | Spécification OpenAPI 3.2.0 |


<p v-click>
  ❌ Swagger Specification
</p>

<p v-click>
  ✅ OpenAPI Specification (OAS)
</p>

<p v-click>
  ❓ Swagger ... ?
</p>

<style>
.strike {
  position: relative;
}

.strike::after {
  content: '';
  position: absolute;
  left: 0;
  top: 50%;
  width: 0%;
  height: 2px;
  background: currentColor;
  transition: width 0.4s ease;
}

.strike.active::after {
  width: 100%;
}
</style>

---
transition: slide-up
level: 2
---

# Mélangé? C'est mélangeant!

<p v-click>
  Swagger est un ensemble de produits de SmartBear utilisant la spécification OpenAPI.
</p>

<p v-click>
  'Swagger' est devenu une antonomase.
</p>

<p v-click>
  Souvent utilisé sans faire de distinction.
</p>

<p v-click>
  Si on parle de Swagger, on peut assumer qu'on parle d'OpenAPI et vice-versa.
</p>

<a href="https://petstore.swagger.io/" v-click>En fait, ceci n'est pas un Swagger</a>

<p v-click>
  C'est un <u>site de documentation</u> généré à partir d'un outil 'swagger-ui' en le nourrissant d'un <strong>document de spécification OpenAPI</strong>.
</p>

<p v-click>
  Ce qu'on va voir, c'est que <strong>'Swagger' est bien plus qu'un site de documentation</strong>.
</p>

<style>
.strike {
  position: relative;
}

.strike::after {
  content: '';
  position: absolute;
  left: 0;
  top: 50%;
  width: 0%;
  height: 2px;
  background: currentColor;
  transition: width 0.4s ease;
}

.strike.active::after {
  width: 100%;
}
</style>