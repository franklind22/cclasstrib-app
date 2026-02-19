```markdown
# cClassTrib por NCM – Reforma Tributária 2026

[![GitHub Pages](https://github.com/franklind22/cclasstrib-app/actions/workflows/pages/pages-build-deployment/badge.svg)](https://franklind22.github.io/cclasstrib-app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Aplicativo web 100% offline** para consultar rapidamente os códigos **cClassTrib**, **CST**, **percentual de redução** e **legislação** dos NCMs conforme a **Lei Complementar 214/2025** (Reforma Tributária – IBS/CBS).

Funciona no navegador (celular e desktop), sem servidor, sem login, sem instalação.

### ✨ Funcionalidades

- Busca instantânea por NCM (2 a 8 dígitos)
- Filtro: Todos / Com redução / Alíquota integral
- Histórico de buscas (salvo no navegador – últimos 10)
- Importação de tabela oficial JSON (formato governo/NF-e)
- Exportação em CSV (com data no nome do arquivo)
- Tabela responsiva com cabeçalho fixo e paginação (20 itens/página)
- Design mobile-first, gradiente header, loading e mensagens claras
- Botão direto para tabela oficial no Portal SVRS
- Busca otimizada com Trie (rápida mesmo com milhares de NCMs)

### 🖥️ Demonstração Online

Acesse agora:

→ **https://franklind22.github.io/cclasstrib-app/**

Exemplos rápidos de busca:
- `96190000` → Absorventes e fraldas (saúde menstrual)
- `48181000` → Papel higiênico (Anexo VIII)
- `34011190` → Sabonete em barra (Anexo VIII)
- `1006` → Arroz (cesta básica)

### 🚀 Como usar (no celular ou computador)

1. Acesse o link acima  
2. Digite o NCM (ex: 9619 ou 4818)  
3. Para tabela completa:  
   - Clique em **“Tabela oficial SVRS”**  
   - Baixe/exporte o JSON do Portal  
   - Importe no app clicando em “Importar JSON”

Funciona offline após primeira carga (exceto atualização via JSON externo).

### 📥 Como atualizar a base completa

1. Acesse o Portal oficial:  
   https://dfe-portal.svrs.rs.gov.br/DFE/TabelaClassificacaoTributaria  
   (versão mais recente: v.1.40 – jan/2026)

2. Consulte/exporte o JSON (pode precisar de certificado digital para download full)

3. No app → clique em “Importar JSON” → selecione o arquivo baixado

### 🛠️ Tecnologias

- HTML5 + CSS3 (Grid, Flex, Gradients, Sticky)
- JavaScript puro (ES5 – compatibilidade máxima com Android antigo)
- Estrutura Trie para busca por prefixo (O(1) rápido)
- localStorage para histórico
- FileReader + Blob para import/export
- Mobile-first + touch-action

### 📄 Estrutura esperada do JSON oficial

```json
{
  "96190000": [
    {
      "cclasstrib": "200013",
      "cst": "200",
      "descricao": "Absorventes higiênicos",
      "pReducao": "100%",
      "pCredPres": "0%",
      "legislacao": "LC214/Anexo VII",
      "regime": "reducao",
      "ativo": true
    }
  ]
}
```

### ⚠️ Aviso importante

Este app **não substitui** consulta oficial na Receita Federal, SEFAZ ou contador.  
Os dados iniciais são exemplificativos e baseados em interpretações públicas da LC 214/2025.  
Sempre valide com a tabela oficial mais recente do governo.

### 📄 Licença

MIT License – use, modifique e distribua livremente.

### 🙏 Contribuições

Quer adicionar mais NCMs, corrigir algo ou melhorar?  
- Abra uma Issue  
- Envie Pull Request  
- Compartilhe com contadores, advogados tributaristas e lojistas!

Feito com ❤️ por **Franklin D.** (@FranklinDalmaso) – São Mateus/ES – 2026
```
