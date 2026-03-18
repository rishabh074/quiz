# quiz


# 🧠 Quiz App (Vue 3 + Vite)

A simple and interactive quiz application built using **Vue 3 (Composition API)** and **Vite**.
Users can answer multiple-choice questions, track progress, and view results at the end.

---

## 🚀 Features

* ✅ Multiple-choice questions
* 📊 Dynamic progress bar
* 🎯 Score tracking (correct answers)
* 🏁 Result screen based on score
* 🔄 Reset quiz functionality
* ⚡ Fast performance with Vite

---

## 🛠️ Tech Stack

* Vue 3 (Composition API)
* Vite
* JavaScript (ES6)
* SCSS

---

## 📂 Project Structure

quiz/
│── public/
│── src/
│   ├── components/
│   │   ├── questions.vue
│   │   ├── results.vue
│   ├── App.vue
│   ├── main.js
│── package.json
│── vite.config.js

---

## 📸 Screenshots

### 🟢 Question Screen

![Question Screen](./screenshots/question.png)

### 📊 Progress Bar

![Progress](./screenshots/progress.png)

### 🏁 Result Screen

![Result](./screenshots/result.png)

---

## ⚙️ Setup Instructions

### Install dependencies

npm install

### Run development server

npm run dev

### Build for production

npm run build

---

## 🔄 How It Works

* User selects an answer
* App checks if it is correct
* Updates:

  * totalCorrect
  * questionsAnswered
* Progress bar updates dynamically
* After last question → results screen is shown

---

## 🎯 Future Improvements

* Add timer per question
* Add categories
* Save score in local storage
* Add animations

---

## 👨‍💻 Author

Rishabh Bedi
Frontend Developer (Vue.js | React | Angular)

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!









This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Recommended Browser Setup

- Chromium-based browsers (Chrome, Edge, Brave, etc.):
  - [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
  - [Turn on Custom Object Formatter in Chrome DevTools](http://bit.ly/object-formatters)
- Firefox:
  - [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
  - [Turn on Custom Object Formatter in Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
