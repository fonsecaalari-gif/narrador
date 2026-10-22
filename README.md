# 🎙️ Narrador com a sua voz

Uma página onde você grava a sua voz uma vez, cola uma história e ouve ela narrada por você, em português. A sua voz e o histórico de narrações ficam salvos no navegador. Não precisa instalar nada nem rodar Python.

São duas partes, as duas grátis:

| Parte | Onde fica | O que faz |
|---|---|---|
| `index.html` | GitHub Pages | A página que você usa: grava a voz, guarda o histórico |
| pasta `servidor/` | Hugging Face Spaces | O "cérebro" que clona a voz e gera o áudio |

A configuração abaixo é feita **uma vez só** (uns 15 minutos).

---

## Parte 1 — Criar o servidor no Hugging Face

1. Crie uma conta grátis em **https://huggingface.co/join**.
2. Vá em **https://huggingface.co/new-space** e preencha:
   - **Space name:** `narrador`
   - **Select the Space SDK:** escolha **Gradio** (e depois **Blank**)
   - **Space hardware:** deixe **CPU basic · Free**
   - **Visibility:** **Public** (mais simples; veja a nota sobre privacidade no fim)
   - Clique em **Create Space**.
3. Na página do Space, clique em **Files** → **+ Add file** → **Upload files**.
4. Arraste os **3 arquivos da pasta `servidor/`** (`app.py`, `requirements.txt` e `README.md`) e clique em **Commit changes to main**.
   - Se ele perguntar se quer substituir o `README.md`, confirme.
5. Clique em **App**. Ele vai mostrar **Building** por uns 5 a 10 minutos (instalando tudo). Quando aparecer a tela do "Servidor do Narrador", está pronto.

O endereço do seu servidor é **seu-usuario/narrador** (aparece no topo da página do Space).

## Parte 2 — Colocar a página no GitHub

1. Entre no **https://github.com** e clique em **New repository** (botão verde ou o **+** no topo).
   - **Repository name:** `narrador`
   - Marque **Public**
   - Clique em **Create repository**.
2. Na tela seguinte, clique no link **uploading an existing file**.
3. Arraste o **`index.html`** e este **`README.md`** e clique em **Commit changes**.
   (A pasta `servidor/` não precisa ir para o GitHub, mas pode enviar também, para ficar guardada.)
4. Vá em **Settings** → **Pages** (menu da esquerda).
   - Em **Branch**, escolha **main** e **/ (root)** e clique em **Save**.
5. Espere 1 ou 2 minutos e recarregue. Vai aparecer o endereço do seu site, algo como
   **https://seu-usuario.github.io/narrador/**

## Parte 3 — Usar

1. Abra o seu site.
2. No passo **1. Servidor**, escreva `seu-usuario/narrador` e clique em **Conectar**.
3. No passo **2. Sua voz**, clique em **Gravar** e leia o texto que aparece na tela (15 a 30 segundos). Pode gravar duas ou três vezes, para ficar mais parecido.
4. No passo **3. Nova história**, cole o texto e clique em **Narrar história**.
5. Quando terminar, a narração aparece no **Histórico**, onde você pode ouvir, baixar ou apagar.

Da próxima vez, é só abrir o site: o servidor, a sua voz e o histórico já estão lá.

---

## Bom saber

- **Velocidade:** o servidor grátis não tem placa de vídeo, então é lento. Conte uns **3 a 6 minutos para cada minuto de áudio**. Deixe a página aberta (e a tela do celular ligada) enquanto ele narra.
- **Primeiro uso do dia:** se o servidor ficar uns dias sem uso, ele "dorme". A página acorda ele sozinha, mas isso leva de 2 a 5 minutos.
- **Onde fica o histórico:** no navegador em que você usou. Em outro celular ou computador, o histórico não aparece (a voz você grava de novo rapidinho). Se limpar os dados do navegador, ele some, então baixe os áudios que quiser guardar.
- **Privacidade:** a gravação da sua voz só fica no seu navegador; ela é enviada ao seu servidor apenas na hora de narrar. Se o Space for público, outra pessoa que descobrir o endereço conseguiria usar o servidor (não a sua voz salva). Para fechar isso, deixe o Space como **Private** (em Settings do Space) e cole um token do Hugging Face no campo "Space privado?" da página. O token se cria em https://huggingface.co/settings/tokens (tipo **Read**).
- **Ficou estranho?** Nos "Ajustes da narração", diminua a **Expressividade** para 0.5. Gravar num lugar silencioso faz muita diferença.
- **Licença:** o modelo de voz (XTTS v2) é para uso pessoal, não comercial. Use apenas a sua voz ou a de quem autorizou.
