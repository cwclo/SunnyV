# 🌞 SunnyV — Template Vue 3 + Vite + Tailwind CSS

Bienvenue dans **SunnyV**, un template simple, moderne et responsive pour créer rapidement des sites vitrines.  
Pensé pour être **léger, modulaire et réutilisable** dans différents projets clients.

> ⚙️ Stack : [Vue 3](https://vuejs.org/) + [Vite](https://vitejs.dev/) + [Tailwind CSS](https://tailwindcss.com/)

---

## ✨ Fonctionnalités

- ⚡️ Vite pour un dev server ultra rapide
- 💅 Tailwind CSS 3 configuré avec PostCSS & Autoprefixer
- 🎨 Layout responsive prêt à l’emploi
- 🎥 Animations au scroll (`IntersectionObserver`)
- 📱 Menu mobile slide-in avec fermeture auto
- 🌐 Scroll fluide avec `href="#..."`

---

## 🚀 Démarrage rapide

### 1. Cloner le projet

```bash
git clone https://github.com/cwclo/SunnyV.git
cd SunnyV
npm install
npm run dev
````


## 🧱 Structure du projet
📦 src/
├── assets/          → Images, tailwind.css
├── components/      → Composants Vue réutilisables (NavLink, FadeInSection, etc.)
├── views/           → Sections du site (Services, Testimonials, Gallery, etc.)
├── App.vue          → Layout principal
└── main.js          → Point d’entrée Vue + directives
