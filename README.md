# TECH_DOCS | Index de Documentation SISR


Ce projet est une plateforme web moderne servant d'index centralisé pour un serveur web de vidéo style "YouTube" réalisées en **BTS SIO SISR**. L'interface adopte un style **Glassmorphism** (effet de verre) avec une ergonomie.



## Aspect du Projet

* **Design Glassmorphism** : Utilisation intensive de `backdrop-filter: blur()` pour un aspect premium et moderne.
* **Recherche Instantanée** : Moteur de filtrage en Vanilla JavaScript sans rechargement de page.
* **Architecture Responsive** : Navigation fluide sur PC et adaptation intelligente sur mobile (Sidebar rétractable).
* **Typographies Tech** : Combinaison de *Oxanium* (SF) et *Quicksand* (Lisibilité).

## Outils

| Composant | Technologie |
| :--- | :--- |
| **Structure** | HTML5 Sémantique |
| **Style** | CSS3 (Grid, Flexbox, Variables) |
| **Logique** | JavaScript ES6 (Vanilla) |
| **Icônes** | Lucide Icons & Font-Awesome 6 |


## ⚙️ Installation & Déploiement

1.  **Localement** :
    ```bash
    git clone [https://github.com/nathanlempereur/nom-du-repo.git](https://github.com/nathanlempereur/VideoTube.git)
    open index.html
    ```

2.  **Hébergement** : 
    Le projet est entièrement statique et compatible à 100% avec **GitHub Pages**. 
    * Allez dans les `Settings` de votre dépôt.
    * Section `Pages`.
    * Sélectionnez la branche `main` et le dossier `/ (root)`.
    * Votre site est en ligne en quelques secondes.
  
    Ou Installez le sur un serveur Apache2 dans votre répertoire `/var/www/html`, aucun mod supplémentaire n'es nécessaire. 


## Aperçu de la Logique JS

Le filtrage dynamique fonctionne via un écouteur d'événement sur la barre de recherche. Il scanne en temps réel le contenu textuel de chaque carte (`.doc-card`) et ajuste la propriété `display`.

```JavaScript
const searchInput = document.getElementById('searchInput');
const cards = document.querySelectorAll('.doc-card');

searchInput.addEventListener('input', (e) => {
    const val = e.target.value.toLowerCase().trim();
    cards.forEach(card => {
        const isMatch = card.innerText.toLowerCase().includes(val);
        card.style.display = isMatch ? 'block' : 'none';
    });
});
```

## Contribution & Licence 

**Nathan Lempereur** - Étudiant en BTS SIO SISR
* [GitHub](https://github.com/nathanlempereur)
* [LinkedIn](https://www.linkedin.com/in/nathan-lempereur-989624373)
* [Site Web](https://nlempereur.ovh)

Ce projet a été conçu dans un but pédagogique et est Open-Source, vous pouvez le modifier, l’améliorer et proposer des mises à jour.
---

© 2025 Nathan Lempereur — Tous droits réservés
