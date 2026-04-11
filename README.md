# 📦 Sistema de Gerenciamento de Entregas

Sistema interno para controle de encomendas, moradores e porteiros de condomínio. Roda diretamente no navegador — sem servidor, sem instalação.

---

## ✨ Funcionalidades

### Síndica (administradora)
- Dashboard com visão geral das encomendas e moradores
- Cadastro completo de moradores (com veículos e contatos de emergência)
- Gerenciamento de porteiros (criar, editar, ativar/desativar)
- Histórico completo de encomendas
- Pesquisa rápida por nome, bloco/apartamento ou placa de veículo

### Porteiro
- Pesquisa rápida de moradores e veículos
- Registro de entrada de encomendas
- Confirmação de retirada com registro de responsável
- Visualização de encomendas pendentes

---

## 🚀 Como usar

### Opção 1 — Abrir direto no navegador
Baixe o arquivo `index.html` e abra no navegador. Funciona sem internet após o carregamento das fontes.

### Opção 2 — GitHub Pages (recomendado)
Acesse: `https://<seu-usuario>.github.io/<nome-do-repositorio>/`

---

## 🔐 Primeiro acesso

Ao abrir o sistema pela primeira vez:

1. **Passo 1** — Informe o nome do condomínio e o número de blocos
2. **Passo 2** — Crie a conta da síndica (e-mail + senha)

A partir daí, o sistema fica configurado e os dados são salvos automaticamente no navegador (`localStorage`).

> **Atenção:** Os dados ficam armazenados localmente no navegador. Para uso em múltiplos dispositivos ou backup, recomenda-se evoluir para uma solução com banco de dados em nuvem (Firebase, Supabase, etc).

---

## 🏗️ Estrutura do projeto

```
condogest/
└── index.html    # Aplicação completa (HTML + CSS + JS em arquivo único)
```

O sistema foi construído como arquivo único para facilitar o uso sem configuração de ambiente.

---

## 🏢 Estrutura do condomínio suportada

- Blocos: 1 a 12 (configurável no setup)
- Apartamentos: 101–104, 201–204, 301–304, 401–404

---

## 🔍 Pesquisa de veículos

A pesquisa unificada permite buscar por:
- Nome do morador
- Bloco e apartamento (`302`, `bloco 3`, `3/202`)
- Placa de carro ou moto (`ABC-1234`, `abc1234`)
- Modelo do veículo (`civic`, `cg fan`)

Quando o resultado vem de uma placa, ela é destacada visualmente no card.

---

## 📋 Perfis de acesso

| Perfil   | Permissões |
|----------|------------|
| Síndica  | Acesso total — moradores, porteiros, relatórios, configurações |
| Porteiro | Operacional — pesquisa, registrar e confirmar encomendas |

> Moradores **não** têm acesso ao sistema. As comunicações com moradores são feitas via WhatsApp (integração prevista para próxima fase).

---

## 🗺️ Roadmap

- [x] Login com dois perfis (síndica / porteiro)
- [x] Cadastro de moradores com veículos e contatos de emergência
- [x] Gestão de porteiros pela síndica
- [x] Registro e retirada de encomendas
- [x] Pesquisa por nome, apartamento e placa
- [x] Persistência local (localStorage)
- [ ] Notificação via WhatsApp (Twilio API)
- [ ] Upload de foto da encomenda
- [ ] QR Code para retirada
- [ ] Backup / sincronização em nuvem (Firebase)
- [ ] Relatórios e exportação CSV
- [ ] App mobile (React Native + Expo)

---

## 🛠️ Tecnologias

- HTML5 + CSS3 + JavaScript (vanilla)
- Google Fonts — DM Sans + DM Mono
- Armazenamento: `localStorage` do navegador
- Deploy: GitHub Pages

---

## 📄 Licença

MIT — livre para uso e adaptação.
