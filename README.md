# Documentação — Jovem Aprendiz Digital

Documentação de UX/IHC do projeto **Jovem Aprendiz Digital**, plataforma de aprendizado de tecnologia básica para jovens aprendizes de Maceió (disciplina de Interação Humano-Computador).

- **Sistema no ar:** https://jovem-aprendiz-digital.onrender.com/
- **Documentação online:** https://documentacao-jovem-aprendiz-digital.vercel.app/

## Conteúdo

| Arquivo / pasta | O que tem |
| --- | --- |
| [`index.html`](index.html) | Site da documentação UX (página publicada no Vercel) |
| [`SOBRE_O_PROJETO.md`](SOBRE_O_PROJETO.md) | Visão geral e roteiro rápido de navegação do sistema |
| [`DOCUMENTACAO_IHC.md`](DOCUMENTACAO_IHC.md) | Decisões de design, rastreabilidade com o Board UX, WCAG 2 AA e princípios de Norman |
| [`AUDITORIA_UX.md`](AUDITORIA_UX.md) | Diagnóstico de UX que originou os ajustes |
| [`README_TECNICO.md`](README_TECNICO.md) | Arquitetura, modelo de dados e rotas da API |
| [`auditorias/`](auditorias/) | Relatórios Lighthouse, resultados do axe e capturas de antes/depois |

Depois do deploy, os relatórios Lighthouse abrem direto no navegador, por exemplo `/auditorias/dashboard/lighthouse-final`.

## Deploy no Vercel

O site é estático: não tem build nem dependências.

1. Em [vercel.com/new](https://vercel.com/new), importe este repositório.
2. **Framework Preset:** `Other`. Deixe **Build Command** e **Output Directory** vazios (Root Directory: `./`).
3. Clique em **Deploy**.

A configuração fica em [`vercel.json`](vercel.json): URLs sem `.html`, arquivos `.md` servidos como texto UTF-8 e cache para as imagens das auditorias. Cada `git push` na `main` publica uma nova versão.

### Pela linha de comando (opcional)

```bash
npm i -g vercel
vercel        # preview
vercel --prod # produção
```

## Ver localmente

```bash
npx serve .
```
