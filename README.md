# 📋 Multistep Form React

Formulário de avaliação de produto dividido em múltiplas etapas (steps), construído com **React + Vite**. O usuário se identifica, avalia o produto com emojis e comentário, e recebe uma mensagem de agradecimento — tudo com navegação entre etapas e indicador visual de progresso.

🔗 **Demo online:** [forms-multisteps.vercel.app](https://forms-multisteps.vercel.app)

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)

---

## ✨ Funcionalidades

- 🧭 Navegação entre 3 etapas (Identificação → Avaliação → Envio)
- 🔄 Indicador visual de progresso (`Steps.jsx`), destacando a etapa atual e as concluídas
- 😊 Avaliação por emojis (insatisfeito, neutro, satisfeito, muito satisfeito)
- ✅ Validação nativa de campos obrigatórios (`required`)
- 📨 Envio dos dados coletados ao final do fluxo (`handleSubmit`)
- 🎣 Hook customizado (`useForm`) para controlar a etapa atual e a navegação
- 📱 Layout responsivo

## 🛠️ Tecnologias

| Categoria       | Ferramenta |
|-----------------|------------|
| Biblioteca UI   | React |
| Build tool      | Vite |
| Ícones          | React Icons |

## 📁 Estrutura do projeto

```
src/
├── components/
│   ├── UserForm.jsx      # Etapa 1: nome e e-mail
│   ├── ReviewForm.jsx    # Etapa 2: avaliação (emojis) e comentário
│   ├── Thanks.jsx        # Etapa 3: resumo e agradecimento
│   └── Steps.jsx         # Indicador visual das etapas
├── hooks/
│   └── useForm.jsx       # Controla etapa atual, avanço e retrocesso
├── styles/               # CSS de cada componente
├── App.jsx               # Orquestra os componentes, o estado e o envio
└── main.jsx               # Ponto de entrada da aplicação
```

## 🚀 Como rodar localmente

Pré-requisito: [Node.js](https://nodejs.org/) 18+ instalado.

```bash
# Clone o repositório
git clone https://github.com/DevsAlves/forms_multisteps.git
cd forms_multisteps

# Instale as dependências
npm install

# Rode em modo desenvolvimento
npm run dev
```

``` 
Acesse `http://localhost:5173` no navegador.
```

## 📄 Licença
Setup inicial Matheus Battisti
