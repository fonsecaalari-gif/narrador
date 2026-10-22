# 🎙️ Narrador com a sua voz

Grave a sua voz uma vez, cole uma história e ouça ela narrada por você, em português.

**Site:** https://fonsecaalari-gif.github.io/narrador/

## Como usar

1. Abra o site e clique em **Abrir o servidor no Colab**.
2. No Colab, clique em **Ambiente de execução → Executar tudo** (se pedir para entrar na conta Google, entre).
   - Se aparecer um aviso pedindo para **reiniciar a sessão**, aceite e clique em **Executar tudo** de novo.
3. Em uns 5 minutos aparece no Colab o link **"Clique aqui para abrir o seu narrador já conectado"**. Clique nele.
4. Na primeira vez, grave a sua voz no passo **2. Sua voz** (15 a 30 segundos lendo o texto da tela).
5. Cole a história no passo **3** e clique em **Narrar história**. O áudio aparece no **Histórico**.

Da próxima vez, a sua voz e o histórico já estão salvos: é só ligar o Colab (passos 1 a 3) e narrar.

## Bom saber

- **Deixe a aba do Colab aberta** enquanto narra. Quando você fecha ou fica um tempo sem usar, o Colab desliga, mas isso não apaga nada da sua página.
- **O link muda** cada vez que o Colab liga. Por isso, use sempre o link novo que aparece lá.
- **Velocidade:** com a GPU grátis do Colab, cada minuto de áudio leva cerca de 20 a 40 segundos.
- **Onde fica o histórico:** no navegador em que você usa o site. Em outro aparelho ele não aparece, então baixe os áudios que quiser guardar.
- **Ficou estranho?** Nos "Ajustes da narração", diminua a **Expressividade** para 0.5. Gravar num lugar silencioso faz muita diferença.
- **Licença:** o modelo de voz (XTTS v2) é para uso pessoal, não comercial. Use apenas a sua voz ou a de quem autorizou.

## Arquivos

- `index.html`: o site (GitHub Pages).
- `Narrador_servidor.ipynb`: o servidor que roda no Google Colab.
