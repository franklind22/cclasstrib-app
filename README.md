
<div align="center">
  <img src="https://raw.githubusercontent.com/franklind22/cclasstrib-app/main/assets/icon.png" width="100" height="100" alt="Logo"/>
  <h1>🧾 cClassTrib · Consulta NCM</h1>
  <p><strong>Reforma Tributária IBS/CBS · LC 214/2025</strong></p>
  
  <!-- BADGES -->
  <p>
    <img src="https://img.shields.io/badge/versão-4.4-blue" alt="Versão">
    <img src="https://img.shields.io/badge/NCMs-800%2B-green" alt="NCMs">
    <img src="https://img.shields.io/badge/CSTs-154-orange" alt="CSTs">
    <img src="https://img.shields.io/badge/licença-MIT-red" alt="Licença">
    <img src="https://img.shields.io/badge/status-produção-success" alt="Status">
    <img src="https://img.shields.io/badge/HTML-CSS-blue" alt="HTML/CSS">
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black" alt="JavaScript">
    <img src="https://img.shields.io/badge/mobile-friendly-ff69b4" alt="Mobile Friendly">
  </p>

  <!-- LINK DEMO -->
  <h3>
    <a href="https://franklind22.github.io/cclasstrib-app/">
      🚀 ACESSE A DEMO AO VIVO
    </a>
  </h3>
</div>

---

## 📋 **SOBRE O PROJETO**

**cClassTrib** é uma ferramenta de consulta da classificação tributária IBS/CBS por código NCM, baseada na **Lei Complementar 214/2025** — a Reforma Tributária do governo brasileiro.

Desenvolvido para **contadores, profissionais fiscais e empresários**, o sistema oferece:

✅ **Consulta rápida** de NCMs com redução/imunidade  
✅ **Lista completa de CSTs** com documentos fiscais  
✅ **Navegação por capítulos** da NCM  
✅ **Informações oficiais** da LC 214/2025  
✅ **Base de dados validada** com fidelidade à legislação  
✅ **Design 100% responsivo** (funciona perfeitamente em celulares, tablets e desktop)  
✅ **Dark mode** com botão manual (sol/lua)  

---

## ✨ **FUNCIONALIDADES**

### 🔍 **ABA CONSULTA**

| Funcionalidade | Descrição |
|----------------|-----------|
| **Pesquisa por NCM** | Busca por código de 4, 6 ou 8 dígitos (mantendo a exatidão da LC 214/2025) |
| **Busca por capítulo** | Seletor de capítulos NCM - traz TODOS os NCMs do capítulo conforme a lei |
| **Exemplos rápidos** | Clique para testar com ícones ilustrativos |
| **Filtros** | Por CST 200, 410, redução, imunidade (com ícones) |
| **Histórico** | Últimas consultas salvas localmente |
| **Exportação** | Download dos resultados em JSON e CSV |
| **Compartilhamento** | Link com parâmetro `?ncm=XXXX` para compartilhar consultas |
| **Favoritos** | Adicione NCMs aos favoritos com uma estrela ⭐ |

### 📚 **ABA CAPÍTULOS**

| Funcionalidade | Descrição |
|----------------|-----------|
| **Lista completa** | Todos os capítulos NCM com descrição |
| **Contagem de NCMs** | Quantidade por capítulo |
| **Pesquisa** | Filtro por nome ou código |
| **Clique para consultar** | Navegação direta para a aba Consulta |

### 🏷️ **ABA CSTs**

| Funcionalidade | Descrição |
|----------------|-----------|
| **Tabela completa** | 154 registros com cClassTrib |
| **Filtros por grupo** | CST 200, 410 e outros (com ícones) |
| **Pesquisa** | Por CST, cClassTrib ou descrição |
| **Documentos fiscais** | DFes relacionados a cada CST com tooltips |
| **Paginação** | 20 itens por página |
| **Ordenação** | Clique nos cabeçalhos para ordenar |
| **Exportação** | Download da lista completa em JSON |

### ℹ️ **ABA SOBRE**

| Funcionalidade | Descrição |
|----------------|-----------|
| **Estatísticas** | NCMs, regras, versão (com ícones) |
| **Legislação** | Mapeamento dos anexos da LC 214/2025 |
| **Hierarquia NCM** | Explicação sobre níveis (capítulo, posição, subposição, item) |
| **Links úteis** | Acesso direto às fontes oficiais |
| **Aviso legal** | Informações importantes |

---

## 📊 **ESTATÍSTICAS DA BASE**

| Item | Quantidade |
|------|------------|
| **NCMs mapeados** | 800+ |
| **CSTs documentados** | 154 |
| **Anexos da LC 214** | 15 |
| **Documentos fiscais** | 15 tipos diferentes |
| **Capítulos NCM** | 40+ |
| **Níveis hierárquicos** | 4 (capítulo → posição → subposição → item) |

---

## 🗺️ **HIERARQUIA NCM NA BASE DE DADOS**

A base de dados mantém **fidelidade total à LC 214/2025**, respeitando os diferentes níveis de agregação em que a lei se refere aos produtos:

| Nível | Formato | Exemplo | Origem na LC |
|-------|---------|---------|--------------|
| **Capítulo** | `"07"` | Hortaliças | Anexo XV |
| **Posição** | `"0701"` | Batatas | Anexo XV |
| **Subposição** | `"0701.10"` | Batatas para semeadura | Anexo XV |
| **Item** | `"07019000"` | Outras batatas | Criação do sistema (herda da posição) |

### 🎯 **Por que manter diferentes níveis?**

A **Lei Complementar 214/2025** utiliza diferentes níveis de agregação conforme o produto e o benefício. Por exemplo:

- **Anexo I (Cesta Básica)**: Especifica itens de 8 dígitos (`"0201.30.00"`)
- **Anexo XV (Hortifrúti)**: Refere-se a posições inteiras (`"0701"`, `"0803"`)
- **Anexo IX (Insumos Agropecuários)**: Mistura posições (`"2304"`) e subposições (`"2304.00"`)

**Nosso compromisso**: Manter exatamente o código como aparece na lei, garantindo que a interpretação seja a mais fiel possível.

---

## 🛠️ **ESTRUTURA DO JSON**

### Formato Padrão

```json
"NCM": [
  {
    "cclasstrib": "200003",
    "cst": "200",
    "descricao": "Descrição do produto",
    "pReducao": "100%",
    "legislacao": "LC 214/2025 Anexo I",
    "regime": "reducao",
    "documentos": ["NFCE", "NFE"],
    "ativo": true
  }
]
```

### Campos Especiais para Hierarquia

```json
"0701": [
  {
    "cclasstrib": "200014",
    "cst": "200",
    "descricao": "Batatas (posição 0701) - conforme LC 214/2025 Anexo XV",
    "ncm_original": "0701",
    "nivel_ncm": "posicao",
    "abrangencia": "Todos os produtos da posição 0701",
    "pReducao": "100%",
    "legislacao": "LC 214/2025 Anexo XV",
    "regime": "reducao",
    "documentos": ["NFCE", "NFE"],
    "ativo": true
  }
],
"07019000": [
  {
    "cclasstrib": "200014",
    "cst": "200",
    "descricao": "Batatas (outras) - uso específico",
    "herdado_de": "0701",
    "pReducao": "100%",
    "legislacao": "LC 214/2025 Anexo XV (por herança da posição 0701)",
    "regime": "reducao",
    "documentos": ["NFCE", "NFE"],
    "ativo": true
  }
]
```

### Campos Explicados

| Campo | Descrição | Exemplo |
|-------|-----------|---------|
| `cclasstrib` | Código da classificação tributária | `"200003"` |
| `cst` | Código da situação tributária | `"200"` (redução), `"410"` (imunidade) |
| `descricao` | Descrição detalhada do produto | `"Arroz em casca"` |
| `pReducao` | Percentual de redução da base de cálculo | `"100%"`, `"60%"` |
| `legislacao` | Referência legal na LC 214/2025 | `"LC 214/2025 Anexo I"` |
| `regime` | Tipo de benefício | `"reducao"`, `"imunidade"`, `"exclusao"` |
| `documentos` | Tipos de documento fiscal permitidos | `["NFCE", "NFE"]` |
| `nivel_ncm` | Nível hierárquico do NCM | `"capitulo"`, `"posicao"`, `"item"` |
| `herdado_de` | NCM de origem (para itens que herdam benefício) | `"0701"` |
| `ativo` | Se o registro está vigente | `true` |

---

## 📚 **MAPEAMENTO DA LEGISLAÇÃO**

| Anexo | Descrição | Benefício | cClassTrib |
|-------|-----------|-----------|------------|
| **Anexo I** | Cesta Básica | Redução 100% | `200003` |
| **Anexo II** | Serviços de Educação | Redução 60% | `200004` |
| **Anexo III** | Serviços de Saúde | Redução 60% | `200006` |
| **Anexo IV** | Dispositivos Médicos | Redução 60% | `200030` |
| **Anexo V** | Acessibilidade | Redução 60% | `200031` |
| **Anexo VI** | Nutrição Enteral/Parenteral | Redução 60% | `200033` |
| **Anexo VII** | Alimentos | Redução 60% | `200034` |
| **Anexo VIII** | Higiene Pessoal | Redução 60% | `200013` |
| **Anexo IX** | Insumos Agropecuários | Redução 60% | `200038` |
| **Anexo X** | Obras de Arte | Redução 60% | `200039` |
| **Anexo XI** | Defesa e Segurança | Redução 60% | `200043`, `200044` |
| **Anexo XII** | Dispositivos Médicos | Redução 100% | `200004` |
| **Anexo XIII** | Acessibilidade | Redução 100% | `200007` |
| **Anexo XIV** | Medicamentos | Redução 100% | `200009` |
| **Anexo XV** | Hortifrúti | Redução 100% | `200014` |

---

## 🏷️ **CÓDIGOS CST PRINCIPAIS**

| CST | Descrição | Uso | Exemplo |
|-----|-----------|-----|---------|
| **200** | Redução de base de cálculo | Regimes diferenciados | Alimentos, medicamentos |
| **300** | Exportação | Operações de exportação | Todos os produtos |
| **400** | Isenção | Dispensa de pagamento | Casos específicos |
| **410** | Imunidade | Fora do campo de incidência | Livros, jornais, ouro |
| **450** | Suspensão | Pagamento suspenso | Regimes especiais |

---

## 🔧 **CORREÇÕES RECENTES (Versão 4.4)**

### 🔍 **Duplicidades Resolvidas**

| NCM | Problema | Solução |
|-----|----------|---------|
| `"3004"` | Duas entradas conflitantes | Mantida a do Anexo XIV (medicamentos) |
| `"3002"` | Duplicata idêntica | Removida repetição |
| `"3006"` | Duplicata idêntica | Removida repetição |
| `"38210000"` | Conflito Anexo IV vs Anexo IX | Mantida a do Anexo IV (diagnóstico) |
| `"90189099"` | Produtos diferentes no mesmo NCM | Descrições mescladas |

### 📝 **Padronização de Regimes**

- `"exclusao_bc"` → `"exclusao"` (padronizado)
- `"Exclusão BC"` → `"100%"` (padronizado como percentual)
- Adicionado campo `"tipo_beneficio"` para manter detalhamento original

### 🧹 **Documentos Fiscais**

- `"NFCOM"` removido (sigla não padrão)
- Produtos militares agora usam documentos padrão
- Energia elétrica mantém `"NF3E"` (correto)

---

## 🛠️ **TECNOLOGIAS UTILIZADAS**

- HTML5
- CSS3 (com variáveis, design responsivo e media queries otimizadas)
- JavaScript (vanilla, sem dependências)
- JSON para banco de dados
- GitHub Pages para hospedagem
- Font Awesome 6 para ícones

---

## 📁 **ESTRUTURA DO PROJETO**

```
cclasstrib-app/
├── index.html          # Aplicação principal
├── dados.json          # Base de dados dos NCMs (800+ registros)
├── README.md           # Documentação
└── assets/             # Imagens e ícones
    └── icon.png        # Ícone do projeto
```

---

## 🚀 **COMO EXECUTAR LOCALMENTE**

### Opção 1: Abrir direto
1. Clone o repositório:
   ```bash
   git clone https://github.com/franklind22/cclasstrib-app.git
   cd cclasstrib-app
   ```
2. Abra o arquivo `index.html` no navegador

### Opção 2: Servidor local (recomendado)
```bash
npx http-server
# ou
python -m http.server 8080
```
Acesse `http://localhost:8080`

---

## 📖 **COMO ATUALIZAR OS DADOS**

### Para adicionar um novo NCM:

Abra o arquivo `dados.json` e adicione:

```json
"02013000": [
  {
    "cclasstrib": "200003",
    "cst": "200",
    "descricao": "Carnes de bovino, frescas ou refrigeradas, desossadas",
    "pReducao": "100%",
    "legislacao": "LC 214/2025 Anexo I",
    "regime": "reducao",
    "documentos": ["NFCE", "NFE"],
    "ativo": true
  }
]
```

### Para adicionar uma posição (capítulo) como na lei:

```json
"0701": [
  {
    "cclasstrib": "200014",
    "cst": "200",
    "descricao": "Batatas (posição 0701) - conforme LC 214/2025 Anexo XV",
    "ncm_original": "0701",
    "nivel_ncm": "posicao",
    "abrangencia": "Todos os produtos da posição 0701",
    "pReducao": "100%",
    "legislacao": "LC 214/2025 Anexo XV",
    "regime": "reducao",
    "documentos": ["NFCE", "NFE"],
    "ativo": true
  }
]
```

### Para adicionar um novo CST:

No arquivo `index.html`, localize o array `CST_DATABASE` e adicione:

```javascript
{ 
  cst: '200', 
  cclass: '200054', 
  descricao: 'Novo regime tributário', 
  reducao: '60%', 
  documentos: ['NFCE', 'NFE'], 
  anexo: 'XVI' 
}
```

---

## 🔗 **LINKS ÚTEIS**

| Link | Descrição |
|------|-----------|
| [📜 LC 214/2025](https://www.planalto.gov.br/ccivil_03/leis/lcp/lcp214.htm) | Lei Complementar na íntegra |
| [📊 Classificação Tributária SVRS](https://dfe-portal.svrs.rs.gov.br/Cff/ClassificacaoTributaria) | Portal da Conformidade Fácil - RS |
| [🔍 Consulta NCM SEFAZ/RS](https://www.sefaz.rs.gov.br/NFE/NFE-WIZARD_NCM-CON.aspx) | Ferramenta oficial da SEFAZ Rio Grande do Sul |
| [📘 Tabela NCM Completa](https://portalunico.siscomex.gov.br/classif/#/sumario?perfil=publico) | Portal SISCOMEX |
| [🐙 GitHub](https://github.com/franklind22/cclasstrib-app) | Repositório oficial |
| [🚀 Demo](https://franklind22.github.io/cclasstrib-app/) | Versão online |

---

## ⚠️ **AVISO LEGAL**

> **⚠️ Este software é uma ferramenta de consulta e apoio ao desenvolvimento.**  
> Os dados foram consolidados com base na **Lei Complementar 214/2025** e mantêm fidelidade aos códigos NCM conforme publicados na legislação.  
> **Importante**: A lei utiliza diferentes níveis de agregação (capítulos, posições, subposições). Nossa base respeita essa estrutura.  
> **Sempre valide** as informações com um profissional de contabilidade antes de aplicá-las em ambientes de produção fiscal.

---

## 👨‍💻 **DESENVOLVEDOR**

<div align="center">
  <h3>Franklin D22</h3>
  <p>
    <a href="https://github.com/franklind22">
      <img src="https://img.shields.io/badge/GitHub-100000?logo=github&logoColor=white" alt="GitHub" height="30">
    </a>
    <a href="mailto:franklind22@email.com">
      <img src="https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white" alt="Email" height="30">
    </a>
  </p>
</div>

---

## ⭐ **CONTRIBUA**

Se você gostou do projeto:

- ⭐ **Dê uma estrela** no GitHub
- 🐛 **Reporte issues** ou sugira melhorias
- 📢 **Compartilhe** com outros profissionais

---

## 📱 **MOBILE-FRIENDLY**

O app foi totalmente otimizado para dispositivos móveis:

✅ **Scroll horizontal** na tabela de CSTs  
✅ **Filter bar com scroll** em telas pequenas  
✅ **Botões com tamanho adequado** para toque  
✅ **Grids adaptativos** (1 coluna em celular)  
✅ **Atalhos de teclado** aparecem apenas no desktop  
✅ **Menus reorganizados** para melhor visualização  
✅ **Tooltips informativos** em elementos de toque  

---

## 📝 **CHANGELOG**

### Versão 4.4 (Março/2026)
- ✅ Base de dados expandida para 800+ NCMs
- ✅ Correção de duplicidades em `3002`, `3004`, `3006`, `38210000`, `90189099`
- ✅ Padronização de regimes (`exclusao_bc` → `exclusao`)
- ✅ Remoção de `"NFCOM"` dos documentos fiscais
- ✅ Adição de campos hierárquicos (`nivel_ncm`, `herdado_de`)
- ✅ Documentação completa da estrutura hierárquica
- ✅ Mapeamento detalhado dos anexos da LC 214/2025

### Versão 4.3 (Fevereiro/2026)
- ✅ Filtro por capítulo corrigido
- ✅ Mobile-friendly aprimorado
- ✅ Novos exemplos de consulta

---

<div align="center">
  <h3>Feito com ❤️ para a comunidade fiscal brasileira</h3>
  <p>© 2026 · Reforma Tributária LC 214/2025 · Versão 4.4</p>
  <p>
    <img src="https://img.icons8.com/color/48/000000/brazil.png" width="30"/>
  </p>
</div>
```

---

## ✅ **O QUE FOI ATUALIZADO NO README**

| Seção | O que mudou |
|-------|-------------|
| **Versão** | 4.3 → 4.4 |
| **Badges** | Atualizadas |
| **Funcionalidades** | Adicionada "Base de dados validada" |
| **Estatísticas** | NCMs 750+ → 800+ / Anexos 11 → 15 |
| **Nova seção** | **Hierarquia NCM na Base de Dados** (explicando os níveis e por que mantemos códigos de 4, 6 e 8 dígitos) |
| **Estrutura do JSON** | Ampliada com campos especiais (`nivel_ncm`, `herdado_de`) |
| **Mapeamento da Legislação** | Completo, com todos os 15 anexos e cClassTrib |
| **Correções Recentes** | Nova seção detalhando as correções da versão 4.4 |
| **Como atualizar** | Exemplos para adicionar posições (capítulos) como na lei |
| **Links úteis** | Adicionado link da Tabela NCM Completa (SISCOMEX) |
| **Aviso Legal** | Reforçada a explicação sobre os diferentes níveis de agregação |
| **Changelog** | Versão 4.4 detalhada |
