# 🔥 Grelhada Rooftop

> Página de confirmação de presença para o evento **Grelhada Rooftop** — 12 de Setembro de 2026.

## 📅 Sobre o Evento

| | |
|---|---|
| **Nome** | Grelhada Rooftop |
| **Data** | 12 de setembro de 2026 |
| **Horário** | 15:00 — 00:00 |
| **Local** | Lado Gofrech |
| **Preço** | 500$ por pessoa |

---

## 🚀 COMO CONFIGURAR (PASSO A PASSO)

O site usa **Firebase Realtime Database** para que TODOS os dispositivos vejam as mesmas confirmações em tempo real.

### Passo 1: Criar conta Firebase (gratuito)

1. Vai a [https://console.firebase.google.com/](https://console.firebase.google.com/)
2. Clica em **"Add project"**
3. Dá um nome ao projeto (ex: `grelhada-rooftop`)
4. Desativa Google Analytics (não precisas)
5. Clica em **"Create project"**

### Passo 2: Ativar Realtime Database

1. No menu lateral, clica em **"Build" → "Realtime Database"**
2. Clica em **"Create Database"**
3. Escolhe a localização mais próxima (ex: `europe-west1`)
4. Em **"Start in test mode"** → clica **"Next"** → **"Enable"**

### Passo 3: Obter as credenciais

1. No menu lateral, clica no **ícone de engrenagem (⚙️)** → **"Project settings"**
2. Vai ao separador **"General"**
3. Em **"Your apps"**, clica no ícone **"</>"** (Web)
4. Dá um nome à app (ex: `grelhada-web`)
5. Clica em **"Register app"**
6. **Copia o bloco de código `firebaseConfig`** — algo assim:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "grelhada-rooftop.firebaseapp.com",
  databaseURL: "https://grelhada-rooftop-default-rtdb.firebaseio.com",
  projectId: "grelhada-rooftop",
  storageBucket: "grelhada-rooftop.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdef123456"
};
```

### Passo 4: Colar as credenciais no site

1. Abre o ficheiro `index.html` num editor de texto (Notepad, VS Code, etc.)
2. Procura por `const firebaseConfig = {`
3. **Substitui TODOS os valores** pelos teus (copiados no passo anterior)
4. Guarda o ficheiro

### Passo 5: Subir no GitHub Pages

1. Cria um repositório no GitHub
2. Faz upload do `index.html` (diretamente na raiz, não dentro de pasta)
3. Vai a **Settings → Pages**
4. **Source:** Deploy from a branch → **main** → **/ (root)**
5. **Save** e espera 1-2 minutos
6. O link será: `https://o-teu-user.github.io/nome-do-repo/`

---

## 🔐 Acesso Administrativo

- Clica em **🔐 Área do Organizador** no rodapé
- **Senha:** `25575`
- No painel podes ver todos os confirmados, pesquisar, remover e exportar CSV

---

## ⚠️ Nota sobre as regras do Firebase

Por agora a base de dados está em **"modo de teste"** (qualquer pessoa pode ler/escrever). Para um evento real, deves alterar as regras para:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

> ⚠️ Isto é necessário porque o site não tem autenticação de utilizadores — qualquer pessoa precisa de conseguir confirmar presença.

---

## 🛠 Tecnologias

- HTML5 + CSS3 + JavaScript vanilla
- Firebase Realtime Database (sincronização em tempo real)
- Design responsivo (mobile-first)

---

*Criado para a Grelhada Rooftop — 12/09/2026*
