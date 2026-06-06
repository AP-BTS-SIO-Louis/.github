name: 🚀 Pull Request Template
description: Modèle obligatoire pour soumettre des modifications sur l'infrastructure ou le code.
title: "[type]: courte description"
body:
  - type: markdown
    attributes:
      value: |
        Merci de contribuer ! Veuillez remplir ce formulaire pour faciliter la revue de code.

  - type: input
    id: issue-link
    attributes:
      label: 🔗 Issue liée
      description: Spécifiez l'issue associée pour la fermer automatiquement (ex: Closes #12).
      placeholder: "Closes #"
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: 📝 Description des changements
      description: Expliquez de manière concise le contexte, ce que cette PR modifie, et pourquoi.
      placeholder: "Ex: Ajout du rôle Ansible pour sécuriser le cluster K3s..."
    validations:
      required: true

  - type: dropdown
    id: change-type
    attributes:
      label: ⚙️ Type de modification
      description: Quelle est la nature de cette Pull Request ?
      options:
        - "✨ Feature (Nouvelle fonctionnalité / Évolution)"
        - "🐛 Bugfix (Correction d'un dysfonctionnement)"
        - "♻️ Chore / Refactoring (Mise à jour, maintenance)"
        - "⚠️ Breaking Change (Rupture de compatibilité)"
    validations:
      required: true

  - type: checkboxes
    id: dod
    attributes:
      label: ✅ Definition of Done (DoD)
      description: Cochez les critères validés avant de demander la revue de code.
      options:
        - label: Le code a été testé localement et s'exécute sans erreur.
          required: true
        - label: Aucun secret ou clé privée n'est présent (validation TruffleHog).
          required: true
        - label: La documentation (README, .env.example) a été mise à jour.
          required: false