---
transition: fade-out
---

# Exemples de pratiques de travail (*workflow*)

- Code-First
- Design-First


---
---

# Scénario

**Alice**, **Jean** et **Marc** ont besoin d'une nouvelle API.

<div v-click>
Ils veulent être productifs.
</div>

<div v-click>

Alice est développeuse *mobile*.

Marc est développeur *web*.

Jean est développeur *backend*.
</div>

---
---

# Scénario (suite)

## Approche sans utiliser OpenAPI

**Alice**, **Marc** et **Jean** collaborent pour définir le contrat de données.

<div v-click>

🚫 **Alice** et **Marc** sont bloqués.
</div>

<div v-click>

Ils attendent que le serveur de **Jean** soit disponible.
</div>

<div v-click>

⌛ Après plusieurs semaines de travail, **Jean** livre la première version non-stable de l'API.

</div>

<div v-click>

✅ **Alice** et **Marc** peuvent commencer leur travail.

🛜 Ils se connectent au serveur fait par **Jean**.

</div>

<div v-click>

🐌 **Alice** implémente les types et le code nécessaire pour interroger l'API.

🐌 **Marc** implémente les types et le code nécessaire pour interroger l'API.

</div>

---
---

# Scénario (suite)

## Approche sans utiliser OpenAPI

🧬 **Jean** fait évoluer l'API.

<div v-click>

**Alice** et **Marc** ressentent de la friction.

</div>

<div v-click>

Car ils doivent maintenant savoir quoi évoluer dans leur intégration.

Peut-être même recommencer une partie non négligeable de leur travail.

Ce n'est pas facile!

</div>

<div v-click>

🐌 **Jean** ralentit sa cadence de travail pour passer davantage de temps à coordonner avec **Alice** et **Marc**.

</div>

---
---

# Scénario (suite)

## Approche sans utiliser OpenAPI

- 🚫 Il y a eu **des bloquants** qui rajoutent des délais aux livrables.
- 🖨️ Il y a eu une **duplication d'effort**.
- ⏱️ **Un temps et un effort non négligeables** sont passés par les consommateurs à **maintenir leur intégration**.
- Le travail des trois développeurs est très **couplé** et ils ressentent de la **friction**.
- **Peu de collaboration**.

---
---

# Scénario

## Approche avec OpenAPI (Design-First)

**Alice**, **Jean** et **Marc** collaborent pour définir le contrat de données.

<div v-click>

Ils définissent une spec OpenAPI.
</div>

<div v-click>

Après plusieurs itérations, ils arrivent à la première version du contrat.

</div>

<div v-click>

🏎️ À l'aide du contrat, **ils démarrent** leur travail.

</div>

<div v-click>

**Alice** et **Marc** utilisent un outil OpenAPI pour se générer un SDK client.

</div>

<div v-click>

**Alice** utilise [Swagger Codegen](https://github.com/swagger-api/swagger-codegen/tree/3.0.0) pour obtenir un SDK client en Java.

</div>

<div v-click>

**Marc** utilise [openapi-fetch](https://openapi-ts.dev/openapi-fetch/) pour son SDK client en TypeScript.

</div>

---
---
# Scénario (suite)

## Approche avec OpenAPI (Design-First)

Maintenant qu'ils ont la **poutine** pour communiquer avec l'API, ils utilisent [prism](https://github.com/stoplightio/prism) pour démarrer un serveur qui mock l'API.

<div v-click>

En peu de temps, **ils peuvent se focaliser sur ce qui est important pour eux**: avancer leur produit et non développer une intégration.

</div>

<div v-click>

**Ils peuvent commencer à écrire des tests d'intégration.**

</div>

---
---

# Scénario (suite)

## Approche avec OpenAPI (Design-First)

À l'aide du **contrat**, **Jean** commence le développement de l'API.

<div v-click>

Plutôt que de le générer, il **implémente à la main** les modèles, les routes, les opérations, et les validations.

</div>

<div v-click>

Pour l'aider à **s'assurer que l'implémentation est valide**, il utilise la fonctionnalité de *Validation Proxy* de **Prism**.

</div>

<div v-click>

Il utilise la **spec Arazzo** pour l'aider à générer des tests de contrat.

</div>

---
---

# Scénario (suite)

## Approche avec OpenAPI (Design-First)

<div v-click>

**Jean** livre la première version non-stable de l'API.

</div>

<div v-click>

**Alice** et **Marc** se connectent au vrai serveur pour s'assurer de la bonne intégration.

</div>

<div v-click>

Une correction doit se faire sur le contrat de données.

</div>

<div v-click>

**Alice** et **Marc** regénèrent leur SDK puis adaptent leur code en utilisant un serveur mocké.

</div>

<div v-click>

**Jean** corrige l'implémentation du serveur API (si nécessaire) et le livre.

</div>

<div v-click>

Après une vérification sur le vrai serveur, **Alice** et **Marc** livrent leur mise à jour.

</div>

---
---

# Scénario (suite)

## Approche avec OpenAPI (Design-First)

- 🏎️ Il n'y a eu **aucun bloquant** qui a rajouté des délais aux livrables.
- 🖨️ Il n'y a eu **aucune duplication d'effort**.
- 🏎️ Le temps des consommateurs a été utilisé pour faire avancer leurs produits.
- Le travail des trois développeurs **n'était pas couplé** et ils ressentent **peu de friction**.
- **Bonne collaboration**.
