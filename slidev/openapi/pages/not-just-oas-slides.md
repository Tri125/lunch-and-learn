---
transition: fade-out
---

# OpenAPI Initiative

OpenAPI specification n'est qu'une spécification d'une famille.

Chacun répond à des problèmes différents.

- OpenAPI Spec
     - Décris une API HTTP en détail
- AsyncAPI Spec
     - Décris les Architectures événementiel (Event-Driven Architectures - EDA)
     - https://www.asyncapi.com/docs
     - Example iot Streetlights Kafka API 1.0.0: https://editor.swagger.io/
- Arazzo Spec
    - Décris comment plusieurs API fonctionnent ensemble
    - Map la séquence des appels, les *workflows*, les intéractions complexes.
    - Permet l'automatisation de test End-to-End
    - https://swagger.io/blog/the-arazzo-specification-a-deep-dive/

- Overlay Spec
  - Décris des transformation à appliquer sur une spec OpenAPI
  - Cas d'utilisation
       - Génération de traduction
       - Rajoute et améliore la spec qui n'est pas sous ton contrôle
       - Addons
  - https://www.openapis.org/blog/2024/10/22/announcing-overlay-specification