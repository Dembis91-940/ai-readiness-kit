# AI Readiness Kit — Audit + politique IA clé en main pour PME et solos

Kit commercial complet pour un solopreneur français : aide les PME et indépendants à savoir **par où commencer** avec l'IA, à **encadrer l'usage de leurs équipes** (RGPD, confidentialité, cyber) et à **protéger leurs données**.

> ⚠️ **Avant mise en ligne** : remplacez `votre-domaine.fr` par votre vrai domaine (canonical, Open Graph, footer, emails) et personnalisez les mentions légales.

---

## 📦 Contenu du kit

| Fichier | Rôle |
|---|---|
| `index.html` | Landing page premium (violet royal / argent / ivoire) : hero, 3 douleurs, 3 étapes, 3 offres, formulaire EmailJS, livrables, FAQ, footer |
| `outil-audit.html` | **Outil réel** : questionnaire de maturité IA — 20 questions sur 5 axes, scoring JS (0-100), verdict Novice/Explorateur/Stratège/Leader, plan d'action généré, export PDF, envoi du rapport par email, sauvegarde locale |
| `politique-ia-modele.md` | **La politique IA clé en main** : 20 sections + 3 annexes, placeholders `[ENTREPRISE]`, prête à personnaliser |
| `chatbot.js` + `chatbot-config.js` | Chatbot widget autonome (pattern éprouvé) — FAQ + capture de leads via EmailJS |
| `README.md` | Ce fichier |

---

## 💰 Les 3 offres

1. **Audit de maturité IA — 97 €** : questionnaire + score + plan d'action (l'outil en ligne est gratuit pour générer la demande).
2. **Politique IA clé en main — 197 €** (★ le plus choisi) : politique rédigée sur mesure + sensibilisation équipe, livrée en 48-72 h.
3. **Pack Complet — 297 €** : audit + politique + 3 mois d'accompagnement (point mensuel + échanges illimités).

Garantie satisfait ou remboursé 14 jours.

---

## ⚙️ EmailJS (déjà configuré, envoi réel)

Le formulaire de commande, le chatbot et l'envoi du rapport d'audit utilisent EmailJS avec les identifiants existants :

- **Service ID :** `service_cy1ytdb`
- **Template ID :** `template_xpo58cv`
- **Public Key :** `8Pui4ZEqxW2jRVF7h`

Payload envoyé : `{ site, name, email, question }` — avec `site = "AI Readiness Kit"` (ou « AI Readiness Kit — Audit de maturité » pour les rapports).

Pour changer de compte EmailJS : remplacez les 3 valeurs dans `index.html` (script d'init + `emailjs.send`), `outil-audit.html` et `chatbot-config.js`.

---

## 🧭 Fonctionnement de l'outil d'audit

- **5 axes × 4 questions** : Données, Équipes, Outils, Gouvernance, Sécurité.
- Chaque réponse vaut 0 à 3 points → score global **/100** (chaque axe est aussi noté /100).
- **Niveaux** : Novice (< 40) · Explorateur (40-64) · Stratège (65-84) · Leader (≥ 85).
- **Plan d'action** généré dynamiquement : urgences (< 50 par axe) → consolidation → excellence, avec échéances 30/60/90 jours.
- **Export PDF** : bouton « Exporter le rapport » → rendu print local (`window.print`), aucun serveur requis.
- **Sauvegarde locale** : réponses stockées dans `localStorage` (`airk_answers`, `airk_index`, `airk_entreprise`) → reprise possible à tout moment, bouton « Recommencer » pour tout effacer.
- **Envoi par email** : le rapport peut être demandé par email via EmailJS.

> Les réponses ne quittent jamais l'appareil de l'utilisateur (sauf envoi volontaire du rapport par email).

---

## 🎨 Design

- **Palette** : violet royal `#5b21b6` · argent `#cbd5e1` · ivoire `#faf9f7` (+ tons profonds `#2e1065`, `#4c1d95`).
- **Typographie** : Fraunces (titres serif élégants) + Inter (corps).
- **Ambiance** : cabinet de conseil premium — espaces généreux, filets argentés, cartes de score, animations reveal au scroll (IntersectionObserver), micro-interactions.
- **SEO / partage** : schema.org JSON-LD (ProfessionalService + Offres + FAQPage, WebApplication pour l'outil), Open Graph, Twitter Card.
- **Responsive** : mobile-first, menu burger, grilles adaptatives.

---

## 🚀 Mise en ligne

Aucun serveur requis : les deux pages sont 100 % statiques (l'EmailJS et l'export PDF fonctionnent en local comme en ligne).

1. Hébergez le dossier sur n'importe quel hébergement statique (Netlify, Vercel, OVH, GitHub Pages…) — **attention : ce projet n'est pas à publier sur GitHub sans validation.**
2. Personnalisez dans `index.html` :
   - `votre-domaine.fr` (canonical, og:url, og:image, emails du footer) ;
   - nom du cabinet, SIRET, ville dans le footer ;
   - le placeholder `[Nom du cabinet]`.
3. Testez le formulaire (onglet EmailJS → *Email Logs*).
4. Adaptez `politique-ia-modele.md` au client (placeholders `[ENTREPRISE]`…) avant livraison, ou livrez-le tel quel en tant que modèle.

---

## 🔍 Checklist qualité

- [ ] Orthographe française vérifiée
- [ ] Formulaire EmailJS testé (envoi reçu dans la boîte liée au template)
- [ ] Audit : 20 questions, scoring, niveaux, plan d'action, PDF, localStorage testés
- [ ] Chatbot : questions FAQ + capture de leads testés
- [ ] Liens internes (`index.html` ↔ `outil-audit.html`) vérifiés
- [ ] Favicon ajouté si besoin, og:image générée

---

© 2026 AI Readiness Kit — Kit livrable pour solopreneur. Ne pas revendre tel quel.
