# 🚀 FFSIXX

**FFSIXX** é uma biblioteca ultra-leve e poderosa para manipulação de imagens no Node.js, construída sobre o motor do **FFmpeg**. 

Diferente de outras bibliotecas, a FFSIXX trabalha inteiramente com **Buffers e Streams**, sendo perfeita para **Bots (WhatsApp/Telegram)**, ferramentas de CLI e ambientes com recursos limitados como o **Termux**.

![NPM Version](https://img.shields.io/npm/v/ffsixx.svg)
![License](https://img.shields.io/npm/l/ffsixx.svg)
![Downloads](https://img.shields.io/npm/dm/ffsixx.svg)

---

## ✨ Destaques

* **Zero dependências pesadas:** Usa o FFmpeg que você já tem no sistema.
* **Compressão Inteligente:** Define um alvo (ex: 200KB) e a lib ajusta qualidade/escala automaticamente.
* **Bot-Ready:** Ferramentas nativas para criação de **Stickers (WebP)**, **Molduras** e **Filtros**.
* **Branding Ready:** Marca d'água com texto ou logo com controle total de opacidade.
* **Smart Resize:** Modos `cover` (corte inteligente) e `contain` (com fundo customizável).
* **Stream Friendly:** Sem arquivos temporários, tudo processado em memória.
* **TypeScript Ready:** Tipagem completa incluída.

---

## 📦 Instalação

### Pré-requisitos
Certifique-se de ter o **FFmpeg** instalado no sistema:
- **Termux (Android):** `pkg install ffmpeg`
- **Ubuntu/Debian:** `sudo apt install ffmpeg`
- **macOS:** `brew install ffmpeg`

### Instalação do pacote

```bash
npm install ffsixx
```
```bash
pnpm add ffsixx
```

🛠️ Como Usar
1. Compressão Inteligente (Target Size)
Ideal para bots que precisam enviar imagens leves sem perder qualidade visual.

import { compress } from 'ffsixx';
const { buffer, sizeKB } = await compress(img, { maxSizeKB: 300 });

2. Stickers (WhatsApp/Telegram)
import { sticker } from 'ffsixx';
const res = await sticker(buffer, { quality: 80 });

3. Marca d'água (Branding)
import { watermark } from 'ffsixx';
const res = await watermark(buffer, { text: 'SIXX CORE', position: 'bottom-right' });

4. Molduras e Filtros
import { frame, applyFilter } from 'ffsixx';
const moldura = await frame(buffer, { color: 'white' });
const pb = await applyFilter(buffer, 'grayscale');

🔧 API Reference
| Função | Parâmetros Principais | Descrição |
|---|---|---|
| compress | maxSizeKB, mode, format | Comprime até atingir o peso alvo em KB. |
| sticker | quality | Gera WebP (512x512) para figurinhas. |
| frame | color, thickness | Adiciona bordas coloridas à imagem. |
| applyFilter | name | Filtros: grayscale, sepia, invert, dark. |
| watermark | text, logo, position | Aplica texto ou imagem sobre a foto. |
| resize | width, height, fit | Redimensiona (cover, contain, fill). |
| crop | x, y, width, height | Recorta uma área específica. |
| flip / flop | buffer | Espelhamento horizontal e vertical. |
📂 Estrutura de Fontes
Para marcas d'água de texto, mantenha sua fonte em: ./fontes/SNPro-Bold.ttf. Se não encontrada, a lib usará a fonte padrão do sistema.
🤝 Contribuição
 * Faça um Fork do projeto.
 * Crie uma Branch (git checkout -b feature/NovaFeature).
 * Commit suas mudanças (git commit -m 'feat: nova ferramenta').
 * Abra um Pull Request.
📝 Licença
Este projeto está sob a licença MIT.
👤 Autor
Ytsixx
* 🐙 GitHub: [@Ytsixx](https://github.com/Ytsixx)
* 📦 NPM: [ffsixx](https://www.npmjs.com/package/ffsixx)
Desenvolvido com ⚡ por FFSIXX Team
EOF



Agora sim! Desafio pago. O arquivo ficou gigante e com tudo o que a **FFSIXX** oferece.
