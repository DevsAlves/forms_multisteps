# 📋 Multistep Form React

Formulário de avaliação de produto dividido em múltiplas etapas (steps), construído com **React + Vite**. O usuário se identifica, avalia o produto com emojis e comentário, e recebe uma mensagem de agradecimento — tudo com navegação entre etapas e indicador visual de progresso.

🔗 **Demo online:** [forms-multisteps.vercel.app](https://forms-multisteps.vercel.app)

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

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
| Biblioteca UI   | [React 19](https://react.dev/) |
| Build tool      | [Vite 7](https://vite.dev/) |
| Ícones          | [react-icons](https://react-icons.github.io/react-icons/) |
| Lint            | ESLint 9 |

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

Acesse `http://localhost:5173` no navegador.

### Outros scripts disponíveis

```bash
npm run build     # Gera a build de produção em /dist
npm run preview   # Serve a build de produção localmente
npm run lint      # Roda o ESLint no projeto
```

## 🧠 Como funciona (resumo técnico)

O `App.jsx` mantém um único estado `data` (nome, e-mail, avaliação, comentário) e o repassa para cada etapa via props (`data` + `updateFieldHandler`). A troca de etapa é controlada pelo hook `useForm`, que recebe o array de componentes (`formComponents`) e expõe:

- `currentStep` — índice da etapa atual
- `currentComponent` — componente a ser renderizado
- `changeStep(i, evento)` — avança/retrocede, bloqueando índices fora do intervalo
- `isFirstStep` / `isLastStep` — booleans usados para exibir os botões corretos

Ao chegar na última etapa, o botão "Enviar" dispara `handleSubmit`, que registra os dados coletados no console (ponto de partida para integrar com uma API futuramente).

## 📄 Licença

Este projeto está sob a licença MIT.
