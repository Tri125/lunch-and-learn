---
transition: fade-out
---

# Pourquoi OpenAPI existe?

---
---
# Les problèmes qu'OpenAPI règle

- **Documentation incohérente**
     - Chacun documentait à leur manière
- **Difficulté de tester les APIs**
     - Que fait l'API et dans quel scénario?
     - Qu'est-ce que je teste?
- **Manque de collaboration**
     - Mais qu'est-ce qui se paaaasssseee?!

---
---

# Bénéfices

- **Une seule source de vérité décrivant ton API**
- **Documentation auto-générée**
     - Le truc qu'on appelle 'Swagger' à tort en est un exemple.
- **Génération de code client (aussi appelé SDK)**
     - Intégration sans effort
     - C'est tout aussi trivial de se tenir à jour avec l'évolution de l'API
- **Génération de code serveur**
     - Et oui, ce n'est pas juste pour les consommateurs d'API
- **Génération de serveur Mock**
     - Moins de friction entre implémenteur et consommateur
     - L'équipe 'Front' et l'équipe 'Back' peuvent commencer le travail en même temps
     - Ils se synchronisent une fois prêts (no-stress!)
     - Même principe que de mocker les dépendances externes lors des tests
- **Génération de tests**