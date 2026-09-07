# 📱 Au Pair Dashboard (Oficial v2.5) — Instalação no iPhone

Este pacote transforma o app em um **app de tela de início do iPhone** (PWA): ícone próprio, abre em tela cheia, sem barra do Safari, funcionando **100% offline**.

> **Nota honesta sobre .ipa**: o iOS só instala arquivos `.ipa` via App Store/TestFlight — exige conta Apple Developer (US$ 99/ano), macOS com Xcode e revisão da Apple. O pacote PWA é o caminho oficial da Apple para apps web e não precisa de conta nem de computador.

---

## ✅ Caminho recomendado — hospedar e instalar (dados permanentes)

1. **Coloque a pasta em um endereço HTTPS** (o Safari do iPhone só instala PWA de endereço seguro). Opções gratuitas:
   - **GitHub Pages**: suba os arquivos em um repositório público → Settings → Pages;
   - **Netlify Drop**: arraste a pasta em app.netlify.com/drop;
2. No iPhone, abra o endereço no **Safari**;
3. Botão **Compartilhar** (□↑) → **"Adicionar à Tela de Início"** → **Adicionar**.

Pronto: o **Au Pair Dashboard** aparece com ícone próprio, abre em tela cheia e os dados ficam salvos no aparelho — com o **backup automático** do app (3 cópias) como rede de segurança.

## 📂 Caminho sem hospedagem (atenção ao storage)

- Salve `index-oficial.html` no app **Arquivos** do iPhone e abra via um navegador que suporte arquivos locais;
- ⚠️ O iOS pode **apagar dados de sites não instalados** na tela de início após **7 dias sem uso**;
- **Mitigação**: use **Config → Exportar backup** semanalmente (o arquivo JSON restaura tudo).

## 🖥️ Servir da API no PC (rede local)

Com o backend rodando (`server/server.js`), o app também abre em `http://IP-DO-PC:3000/` no Safari do iPhone (mesmo Wi-Fi). Nesse caso o login JWT passa a ser exigido — use o usuário cadastrado no servidor.

---

## 🗂️ Conteúdo do pacote
| Arquivo | Uso |
|---|---|
| `index-oficial.html` | O app completo (Edição Oficial v2.5) |
| `manifest.json` | Identidade do app instalado (nome, cores, ícone) |
| `icons/apple-touch-icon.png` | Ícone que o iOS usa na tela de início |
| `icons/icon-192.png` / `icon-512.png` | Ícones para Android/manifest |

## 💡 Dicas
- Ao publicar em GitHub Pages/Netlify, renomeie `index-oficial.html` para **`index.html`** (a página inicial do endereço abre direto);
- O **backup** (Config → Exportar) gera um JSON com tudo — guarde um no Drive/iCloud;
- A **tradução 🌐** precisa de internet só na primeira tradução de cada texto.
