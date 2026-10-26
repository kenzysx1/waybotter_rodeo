# 🎲 Extensão Dado Selvagem & Ampliações para Owlbear Rodeo 2.0

Esta extensão converte a lógica do bot do Discord para o formato oficial de extensões do **Owlbear Rodeo (OBR 2.0)**.

---

## 📌 Principais Recursos

1. **Dado Selvagem (Roxo)**:
   - 1d6 especial (gera 2 sucessos no 6, 1 no 5, 1 no 4 com vantagem; gera complicação no 1, ou no 2 com desvantagem).
2. **Dados Normais**:
   - Até 12 dados configuráveis.
   - Sucessos no 5 e 6 (ou 4 com vantagem).
   - Complicações no 1 e 2 com desvantagem.
3. **Mecânica de Pagar o Preço (⚖️)**:
   - Se houver Ampliações e Complicações, o botão "Pagar o Preço" permite anular complicações gastando ampliações.
   - Apenas o autor da rolagem pode acionar essa ação.
4. **Sincronização em Tempo Real (Multiplayer)**:
   - Usa `OBR.broadcast` para transmitir o resultado e o histórico para todos os jogadores conectados na sala do Owlbear Rodeo.
   - Envia notificação nativa na tela da mesa quando alguém rola os dados.
5. **Renderização Visual dos Dados**:
   - Dados fiéis ao design original com posições reais de pips (pontos), cores destacadas (Roxo para selvagem, Verde para sucesso, Vermelho para complicação, Cinza para neutro).

---

## 🚀 Como testar localmente

Você pode abrir o arquivo `index.html` diretamente em qualquer navegador para testar a interface e a mecânica de rolagem (modo local com fallback automático).

Se quiser testar com um servidor local:
```bash
cd owlbear-dice-roller
python -m http.server 8000
```
Acesse `http://localhost:8000`.

---

## 🌐 Como colocar no Owlbear Rodeo (Hospedagem Gratuita)

O Owlbear Rodeo carrega extensões através de uma URL pública segura (`https://`) que contenha o arquivo `manifest.json`.

### Opção 1: GitHub Pages (Recomendado & Grátis)
1. Crie um repositório no GitHub (ex: `dado-selvagem-obr`).
2. Envie os arquivos desta pasta (`manifest.json`, `index.html`, `icon.svg`).
3. Vá em **Settings** > **Pages** e selecione a branch `main` e a pasta `/root`.
4. Salve. O GitHub fornecerá uma URL pública, por exemplo:
   `https://seu-usuario.github.io/dado-selvagem-obr/manifest.json`

### Opção 2: Vercel ou Netlify (Arrastar e Soltar)
1. Crie uma conta gratuita na [Vercel](https://vercel.com) ou [Netlify](https://netlify.com).
2. Arraste a pasta `owlbear-dice-roller` para fazer o deploy instantâneo.
3. Você receberá um domínio HTTPS (ex: `https://meu-dado.vercel.app/manifest.json`).

---

## ⚙️ Como Ativar no Owlbear Rodeo

1. Entre na sua sala no **Owlbear Rodeo** (https://owlbear.rodeo).
2. No canto inferior esquerdo ou no menu de extensões (ícone de quebra-cabeça 🧩 ou Configurações > Extensions), clique em **Add Extension / Instalar Extensão**.
3. Cole a URL do seu `manifest.json` (ex: `https://seu-usuario.github.io/dado-selvagem-obr/manifest.json`).
4. Clique em **Install**.
5. Um novo ícone de dado roxo aparecerá na sua barra de ferramentas ou menu de ações. Ao clicar nele, o painel do rolador se abrirá!
