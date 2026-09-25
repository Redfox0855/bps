# Outlook QR / Code

Petite page web permettant d'ouvrir un nouveau message Outlook à partir d'un code.

## 1. Utilisation par code

Ouvrir :

`index.html`

puis saisir par exemple :

`POL-001`

## 2. Utilisation par QR code

Une fois le site publié, créer un QR contenant une URL comme :

`https://votre-domaine.ch/?code=POL-001`

Lors du scan, la page récupère automatiquement le code et lance le lien `mailto:`.

## 3. Configuration

Modifier la constante `CODES` dans `index.html`.

Exemple :

```javascript
"POL-003": {
  to: "destinataire@exemple.ch",
  cc: "copie@exemple.ch",
  subject: "Objet du message",
  body: "Bonjour,\n\nTexte du message.\n\nSalutations"
}
```

Pour plusieurs destinataires :

```javascript
to: "personne1@exemple.ch;personne2@exemple.ch"
```

Pour plusieurs personnes en copie :

```javascript
cc: "personne1@exemple.ch;personne2@exemple.ch"
```

## 4. Outlook sur Windows

Pour que le bouton ouvre automatiquement Outlook, Windows doit avoir Outlook configuré comme application associée au protocole `MAILTO`.

Avec Outlook classique, cela se règle dans les applications par défaut de Windows.
