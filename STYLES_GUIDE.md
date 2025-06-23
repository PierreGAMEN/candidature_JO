# Guide des Styles Globaux - Candidature JO 2030

## 📝 Vue d'ensemble

Ce projet utilise désormais un système de styles globaux centralisés pour assurer la cohérence visuelle et faciliter la maintenance. Tous les styles récurrents sont définis dans `src/assets/main.css`.

## 🎨 Variables CSS Globales

### Espacements
```css
--spacing-xs: 0.5rem;
--spacing-sm: 0.75rem;
--spacing-md: 1.5rem;
--spacing-lg: 2.5rem;
--spacing-xl: 3.5rem;
```

### Border-radius
```css
--border-radius: 12px;
--border-radius-lg: 16px;
--border-radius-xl: 24px;
```

### Couleurs de texte
```css
--text-primary: #2c3e50;
--text-secondary: #6c757d;
--text-muted: #64748b;
--text-light: #94a3b8;
```

### Transitions
```css
--transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
--transition-fast: all 0.2s ease;
```

### Ombres
```css
--shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.04);
--shadow-md: 0 4px 16px rgba(0, 0, 0, 0.08);
--shadow-lg: 0 8px 25px rgba(0, 0, 0, 0.12);
```

## ✨ Éléments Stylisés Globalement

### 1. Éléments mis en valeur (`<strong>`)

**Usage automatique :**
```html
<strong>Texte important</strong>
```

**Classe utilitaire :**
```html
<span class="highlight">Texte mis en valeur</span>
```

**Propriétés appliquées :**
- Couleur : `#0f0d76`
- Font-weight : `600`
- Background dégradé subtil
- Padding et border-radius légers

### 2. Citations (`<blockquote>`)

#### Style principal
```html
<blockquote class="blockquote-main">
    <p>Citation ou message important...</p>
</blockquote>
```

**Ou simplement :**
```html
<blockquote>
    <p>Citation...</p>
</blockquote>
```

**Caractéristiques :**
- Background dégradé clair
- Bordure colorée en haut
- Police italique
- Responsive design
- Ombre subtile

## 🚀 Utilisation dans les Composants

### Exemples d'implémentation

**Values.vue :**
```html
<blockquote class="blockquote-main">
    Mon engagement : mettre mon expérience au service de Jeux exemplaires...
</blockquote>
```

**Adventure.vue :**
```html
<blockquote class="blockquote-main">
    Mon engagement : mettre toute mon énergie au service de Jeux exemplaires...
</blockquote>
```

**Contact.vue :**
```html
<p>Je suis convaincu que la réussite passera par des <strong>femmes et des hommes engagés</strong>...</p>
```

## 📱 Responsive Design

Les styles globaux incluent automatiquement le responsive design :

- **Desktop** : Tailles et espacements complets
- **Tablet (≤768px)** : Tailles réduites, padding adapté
- **Mobile (≤480px)** : Polices plus petites, espacements optimisés

## 🔧 Maintenance

### Avantages du système actuel
1. **Cohérence** : Tous les éléments similaires ont le même style
2. **Maintenabilité** : Une seule modification dans `main.css` s'applique partout
3. **Performance** : Réduction du CSS dupliqué
4. **Flexibilité** : Variables CSS facilement ajustables

### Bonnes pratiques
- Utiliser les variables CSS plutôt que des valeurs hardcodées
- Préférer les classes globales aux styles locaux pour les éléments récurrents
- Documenter les nouveaux styles globaux dans ce guide

## 🎯 Styles Supprimés

Les styles suivants ont été centralisés et supprimés des composants :
- **Marges hardcodées** : Remplacées par les variables `--spacing-*`
- **Bordures et ombres** : Harmonisées avec les variables globales
- **Transitions** : Uniformisées avec `var(--transition)`
- **Styles redondants** : `.engagement` non utilisé dans Values.vue
- **Variables CSS redéfinies** : Suppression des redéfinitions dans les media queries

## 🔄 Migration Future

Pour ajouter de nouveaux styles globaux :
1. Définir les variables CSS dans `:root`
2. Créer le style global dans `main.css`
3. Documenter l'usage dans ce guide
4. Remplacer les styles locaux par la classe globale
5. Tester sur tous les écrans (responsive)
