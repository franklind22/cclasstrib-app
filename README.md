```markdown
# cClassTrib por NCM – Reforma Tributária 2026

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue?logo=githubpages)](https://franklind22.github.io/cclasstrib-app/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)

**Aplicativo web 100% offline-capaz** para consulta rápida de códigos **cClassTrib**, CST, percentual de redução e regime tributário do IBS/CBS conforme a **Lei Complementar 214/2025** (Reforma Tributária).

Funciona diretamente no navegador (desktop e mobile), sem necessidade de servidor backend.

## ✨ Funcionalidades

- Busca por NCM (2 a 8 dígitos) com autocomplete instantâneo
- Filtro: Todos / Apenas com redução / Apenas alíquota integral
- Histórico de buscas salvas no navegador (localStorage – últimos 10)
- Importação de tabela oficial JSON (formato governo / NF-e)
- Exportação em CSV (com data no nome do arquivo)
- Paginação inteligente (20 itens por página)
- Tabela responsiva com cabeçalho fixo (sticky header)
- Loading indicator e mensagens de erro/sucesso claras
- Design moderno, mobile-first, gradiente header, botões coloridos
- Algoritmo de busca por prefixo (Trie) → performance excelente mesmo com +10.000 NCMs

## 🖥️ Demonstração

Acesse a versão online hospedada no GitHub Pages:

→ https://franklind22.github.io/cclasstrib-app/

(Após publicar, substitua pelo link real do seu repositório)

Exemplos de buscas rápidas:

- `96190000` → Absorventes e fraldas (saúde menstrual)
- `48181000` → Papel higiênico (Anexo VIII)
- `30022000` → Vacinas humanas (Anexo XIV)
- `1006` → Todos os tipos de arroz da cesta básica

## 🚀 Como usar localmente

1. Baixe ou clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/cclasstrib-app.git
   ```

2. Abra o arquivo `index.html` diretamente no navegador (Chrome, Firefox, Edge, Safari)

   Ou use Live Server no VS Code / extensão HTML Preview no celular.

3. (Opcional) Para atualizar a base de dados automaticamente:
   - Coloque um arquivo `data.json` no repositório
   - O app tenta carregar via fetch na inicialização

## 📥 Importar tabela oficial completa

1. Baixe a tabela oficial mais recente:
   - Portal NF-e → Diversos → Informe Técnico RT 2025.002 (ou versão mais atual)
   - Ou sites agregadores: SVRS, Taxcel, ALT+C, etc.
   - Formato esperado: `{ "NCM8digitos": [ {cclasstrib: "...", cst: "...", ...} ] }`

2. Clique em “Importar JSON” no app e selecione o arquivo.

## 🛠️ Tecnologias utilizadas

- HTML5 semântico
- CSS3 (Grid, Flexbox, Gradients, Sticky positioning)
- JavaScript puro (ES5 – máxima compatibilidade)
- Estrutura Trie para busca ultra-rápida por prefixo
- localStorage para histórico persistente
- FileReader + Blob API para import/export
- Mobile-first + touch-action: manipulation

## 📊 Estrutura do JSON oficial (esperado)

```json
{
  "96190000": [
    {
      "cclasstrib": "200013",
      "cst": "200",
      "descricao": "Absorventes higiênicos femininos",
      "pReducao": "100%",
      "pCredPres": "0%",
      "legislacao": "LC214/Anexo VII",
      "regime": "reducao",
      "ativo": true
    }
  ],
  "48181000": [
    {
      "cclasstrib": "100001",
      "cst": "200",
      "descricao": "Papel higiênico",
      "pReducao": "60%",
      "pCredPres": "0%",
      "legislacao": "LC214/Anexo VIII",
      "regime": "reducao",
      "ativo": true
    }
  ]
}
```

## 📌 Requisitos mínimos

- Qualquer navegador moderno (Chrome 80+, Firefox 78+, Safari 14+, Edge 80+)
- Android/iOS com navegador atualizado
- Funciona offline após primeira carga (exceto atualização via JSON externo)

## ⚠️ Aviso legal

Este aplicativo **não substitui** consulta oficial junto à Receita Federal do Brasil, SEFAZ ou contador.  
Os dados iniciais são exemplificativos e baseados em interpretações públicas da LC 214/2025 até fevereiro/2026.  
Sempre valide com a tabela oficial mais recente publicada pelo governo.

## 📄 Licença

MIT License – sinta-se à vontade para usar, modificar e distribuir.

## 🙏 Agradecimentos / Contribuições

Contribuições são bem-vindas!  
- Reporte bugs → Issues  
- Sugira mais NCMs ou melhorias → Pull Requests  
- Compartilhe com contadores, advogados tributaristas e lojistas

Feito com ❤️ por Franklin D. (@FranklinDalmaso) – São Mateus/ES – 2026
```
##
