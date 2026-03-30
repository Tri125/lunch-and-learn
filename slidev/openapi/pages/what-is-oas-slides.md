---
transition: fade-out
---

# Qu'est-ce que la spécification OpenAPI?

<div class="max-h-80 overflow-auto">

```yaml
openapi: 3.1.0
info:
  title: Weather API
  description: API for all of your weather prediction.
  version: 0.1.0

servers:
  - url: http://poutine.api.example.com/v1
    description: Weather Server for the North America region
  - url: http://stroopwafel.api.example.com/v1
    description: Weather Server for the Europe region

paths:
  /forecast:
    get:
      summary: Returns the temperature forecast for the next 7 days
      responses:
        "200": # status code
          description: A JSON array of the prediction in celsius
          content:
            application/json:
              schema:
                type: array
                items:
                  type: number
```
</div>
<!-- Footer -->

La définition peut être en YAML ou en JSON.

[Learn more](https://swagger.io/docs/specification/v3_0/basic-structure/)

<!-- Inline style -->
<style>
.footnotes-sep {
  @apply mt-5 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---
---

# Principes

- **Le contrat des données est citoyen de première classe**
- **Contract-First API design**
- **Le contrat est ton artifact le plus important**

<br>

****

Composantes clés

- **Information générale de l'API**
- **Les opérations (GET, POST, etc.)**
- **Les paramètres et les corps de requêtes**
- **Les réponses**
- **L'authentification**