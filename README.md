# Grifo Tools — Conversor & Compressor WebP (MVP)


App 100% client‑side (HTML+CSS+JS) para converter PNG/JPEG/WebP → **WebP** com controle de qualidade, redimensionamento opcional, progresso por etapas, downloads individuais e **ZIP**. Nenhum arquivo é enviado para servidor.


## Recursos
- Conversão via `canvas.toBlob('image/webp', quality)`
- Lotes com **concorrência fixa** (padrão 3)
- Progresso por etapas: 20% (carregar), 50% (resize), 90% (compress), 100% (final)
- **Presets** no `localStorage`
- **ZIP** com JSZip
- Acessível (aria-live, foco visível) e responsivo (barra de ações sticky no mobile)


## Limites recomendados
- Até **500** arquivos por lote
- Até **50–100 MB** por arquivo (teto: 100MB)
- Máx. **12.000 px** no maior lado (se *Redimensionar* desligado e exceder, o app bloqueia)
- ZIP final preferencialmente **< 500 MB**


## Como usar
1. Abra `index.html` no navegador (ou acesse via GitHub Pages).
2. Arraste/solte suas imagens ou clique em **Selecionar arquivos**.
3. Ajuste **Qualidade**, **Redimensionar** (opcional), **Concorrência** (avançado).
4. Clique **Converter**. Acompanhe o progresso por arquivo e total.
5. Use **Baixar** (individual) ou **Baixar ZIP** para tudo.


> **Privacidade:** nenhum upload é feito. O uso de CDNs (Tailwind/JSZip) ocorre apenas para carregar as bibliotecas.

> Dica: se a página não abrir, limpe cache do navegador ou verifique **Settings → Pages** por erros.


---


## Troubleshooting
- **WebP não suportado**: use Chrome/Edge/Firefox/Safari atualizados.
- **Arquivos muito grandes**: reduza a dimensão ou habilite *Redimensionar*.
- **ZIP enorme**: baixe individualmente ou reduza a qualidade.
- **iOS (drag & drop)**: use o botão **Selecionar arquivos**.


## Licença
feito por Thales Pacheco
Uso interno Grifo Agency (MVP). Ajuste conforme necessidade.
