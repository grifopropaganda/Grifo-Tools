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


---


## Publicar no GitHub Pages — Passo a passo


> **Pré‑requisito:** você precisa de uma conta GitHub.


### A) Criar o repositório
1. No GitHub, clique em **New repository**.
2. Nomeie como, por exemplo, `img-webp-tools` (pode ser outro).
3. Selecione **Public**.
4. Clique **Create repository**.


### B) Subir os arquivos
1. No repositório, clique em **Add file → Upload files**.
2. Envie estes arquivos:
- `index.html`
- `logo.png` (placeholder, qualquer PNG; pode trocar depois)
- `.nojekyll` (arquivo **vazio**)
- `README.md`
- *(Opcional)* `CNAME` (apenas se for usar domínio próprio)
3. Clique **Commit changes**.


### C) Ativar o GitHub Pages
1. Vá em **Settings → Pages**.
2. Em **Build and deployment**, em **Source**, selecione **Deploy from a branch**.
3. Em **Branch**, selecione `main` e a pasta `/ (root)`.
4. Clique **Save**.
5. Aguarde alguns instantes até o deploy.
6. A URL pública aparecerá ali (algo como `https://seu-usuario.github.io/img-webp-tools/`).


### D) (Opcional) Domínio personalizado
1. Crie um arquivo **CNAME** na raiz do repo contendo apenas o domínio, por ex.: `imgtools.grifo.agency`.
2. No provedor DNS do seu domínio, crie um **CNAME** apontando **imgtools** → `seu-usuario.github.io`.
3. Aguarde a propagação DNS (pode levar alguns minutos).


> Dica: se a página não abrir, limpe cache do navegador ou verifique **Settings → Pages** por erros.


---


## Troubleshooting
- **WebP não suportado**: use Chrome/Edge/Firefox/Safari atualizados.
- **Arquivos muito grandes**: reduza a dimensão ou habilite *Redimensionar*.
- **ZIP enorme**: baixe individualmente ou reduza a qualidade.
- **iOS (drag & drop)**: use o botão **Selecionar arquivos**.


## Licença
Uso interno Grifo Agency (MVP). Ajuste conforme necessidade.
