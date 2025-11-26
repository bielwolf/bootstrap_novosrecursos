# Instruções para Agentes AI - Projeto Serenatto

## Visão Geral do Projeto
Este é um site responsivo para "Serenatto", uma cafeteria/padaria, desenvolvido com **Bootstrap 5.3.0** e HTML/CSS puro. O projeto é um exercício Alura focado em componentização Bootstrap e design responsivo, sem dependências externas além do CDN.

## Arquitetura & Estrutura

### Camadas Principais
- **HTML (`index.html`)**: Único ponto de entrada; estrutura semântica com Bootstrap
- **CSS (`estilos.css`)**: Customizações e variáveis de tema (cores corporativas)
- **Assets (`assets/`)**: Imagens PNG para banners, cards de produtos, e logo

### Paleta de Cores (CSS Variables)
Definida em `estilos.css`:
```css
--bege: #E6E0D6;           /* cor principal de fundo *)
--marrom-escuro: #816D4F;  /* acentos escuros *)
--marrom-claro: #B29463;   /* acentos claros *)
```

## Padrões & Convenções

### Bootstrap Customization
- Usar classes Bootstrap padrão (`.container`, `.row`, `.col-*`, `.btn`, etc.)
- Estilos customizados em `estilos.css` devem **estender**, não substituir classes Bootstrap
- Nunca sobrescrever CSS do CDN inline no HTML

### Responsividade
- Bootstrap grid system é responsável por breakpoints
- Uso de `col-md-*`, `col-lg-*`, etc. para layouts adaptativos
- Imagens em `assets/` otimizadas para mobile-first

### Nomeação de Componentes
- Cards de produtos: `*-card.png` (ex: `cafe-card.png`)
- Banners: `banner-1.png`, `banner-2.png`, etc.
- Ícones: Via Bootstrap Icons CDN (`.bi` classes)

## Dependências Externas

### CDN (via jsdelivr.net)
- **Bootstrap CSS**: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css`
- **Bootstrap JS Bundle**: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/js/bootstrap.bundle.min.js`
- **Bootstrap Icons**: `https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.4/font/bootstrap-icons.css`

**Nota**: Manter versões fixas para evitar quebras de layout. CDNs carregados via HTTPS com SRI (Subresource Integrity).

## Padrões de Desenvolvimento

### Modificar Estilos
1. Adicionar em `estilos.css`, não inline no HTML
2. Usar variáveis CSS quando aplicável (`:root` ou `body`)
3. Exemplo: uso de `--marrom-escuro` para elementos consistentes com tema

### Adicionar Conteúdo
1. Estrutura semântica HTML5 (usar `<section>`, `<article>`, `<nav>`, etc.)
2. Combinar com classes Bootstrap (`.container`, `.card`, `.btn-primary`)
3. Imagens referenciar em `assets/`

### Acessibilidade
- Usar atributo `lang="pt-br"` no HTML (já configurado)
- Meta viewport para mobile (já configurado)
- Favicon duplo (favicon.png nos assets)

## Fluxo de Trabalho Local

### Visualizar Mudanças
- Abrir `index.html` diretamente no navegador (sem servidor necessário)
- Atualizar com F5 para ver mudanças em CSS

### Adicionar Novos Componentes Bootstrap
1. Consultar [Bootstrap 5 Docs](https://getbootstrap.com/docs/5.3/)
2. Copiar estrutura HTML
3. Customizar em `estilos.css` se necessário

## Checklist para PRs/Changes

- [ ] Classes Bootstrap usadas corretamente
- [ ] Estilos customizados em `estilos.css` (não inline)
- [ ] Imagens otimizadas e referenciadas em `assets/`
- [ ] Responsividade testada (mobile, tablet, desktop)
- [ ] Metadata HTML e favicon corretos
- [ ] SRI integrity hashes do CDN atualizadas se versão mudar
