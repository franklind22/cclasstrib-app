
<div align="center">
  <img src="https://raw.githubusercontent.com/franklind22/cclasstrib-app/main/assets/icon.png" width="80" height="80" alt="Logo"/>
  <h1>🧾 cClassTrib · Consulta NCM</h1>
  <p><strong>Reforma Tributária IBS/CBS · LC 214/2025</strong></p>
  
  <!-- BADGES -->
  <p>
    <img src="https://img.shields.io/badge/versão-4.3-blue" alt="Versão">
    <img src="https://img.shields.io/badge/NCMs-750%2B-green" alt="NCMs">
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
✅ **Design 100% responsivo** (funciona perfeitamente em celulares, tablets e desktop)  
✅ **Dark mode** com botão manual (sol/lua)  

---

## ✨ **FUNCIONALIDADES**

### 🔍 **ABA CONSULTA**

| Funcionalidade | Descrição |
|----------------|-----------|
| **Pesquisa por NCM** | Busca por código de 4, 6 ou 8 dígitos |
| **Busca por capítulo** | Seletor de capítulos NCM - agora traz TODOS os NCMs do capítulo |
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
| **Links úteis** | Acesso direto às fontes oficiais (LC 214, SVRS, SEFAZ/RS, GitHub) |
| **Aviso legal** | Informações importantes |

---

## 📊 **ESTATÍSTICAS DA BASE**

| Item | Quantidade |
|------|------------|
| **NCMs mapeados** | 750+ |
| **CSTs documentados** | 154 |
| **Anexos da LC 214** | 11 |
| **Documentos fiscais** | 15 tipos diferentes |
| **Capítulos NCM** | 40+ |

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
├── dados.json          # Base de dados dos NCMs
├── README.md           # Documentação
└── assets/             # (opcional) Imagens e ícones
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

### Para adicionar um novo CST:

No arquivo `index.html`, localize o array `CST_DATABASE` e adicione:

```javascript
{ 
  cst: '200', 
  cclass: '200054', 
  descricao: 'Novo regime tributário', 
  reducaoIBS: '60%', 
  reducaoCBS: '60%', 
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
| [🐙 GitHub](https://github.com/franklind22/cclasstrib-app) | Repositório oficial |
| [🚀 Demo](https://franklind22.github.io/cclasstrib-app/) | Versão online |

---

## 📚 **MAPEAMENTO DA LEGISLAÇÃO**

| Anexo | Descrição | Benefício |
|-------|-----------|-----------|
| **Anexo I** | Cesta Básica | Redução 100% |
| **Anexo II** | Serviços de Educação | Redução 60% |
| **Anexo III** | Serviços de Saúde | Redução 60% |
| **Anexo IV** | Dispositivos Médicos | Redução 60% |
| **Anexo V** | Acessibilidade | Redução 60% |
| **Anexo VI** | Nutrição Enteral/Parenteral | Redução 60% |
| **Anexo VII** | Alimentos | Redução 60% |
| **Anexo VIII** | Higiene Pessoal | Redução 60% |
| **Anexo IX** | Insumos Agropecuários | Redução 60% |
| **Anexo XII** | Dispositivos Médicos | Redução 100% |
| **Anexo XIII** | Acessibilidade | Redução 100% |
| **Anexo XIV** | Medicamentos | Redução 100% |
| **Anexo XV** | Hortifrúti | Redução 100% |

---

## 🏷️ **CÓDIGOS CST**

| CST | Descrição | Uso |
|-----|-----------|-----|
| **200** | Redução de alíquota | Regimes diferenciados |
| **300** | Exportação | Operações de exportação |
| **400** | Isenção | Dispensa de pagamento |
| **410** | Imunidade | Fora do campo de incidência |
| **450** | Suspensão | Pagamento suspenso |

---

## ⚠️ **AVISO LEGAL**

> **⚠️ Este software é uma ferramenta de simulação pedagógica e de apoio ao desenvolvimento.**  
> Os dados devem ser validados por um profissional de contabilidade antes de serem aplicados em ambientes de produção fiscal.

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

---

<div align="center">
  <h3>Feito com ❤️ para a comunidade fiscal brasileira</h3>
  <p>© 2026 · Reforma Tributária LC 214/2025 · Versão 4.3</p>
  <p>
    <img src="https://img.icons8.com/color/48/000000/brazil.png" width="30"/>
  </p>
</div>
```

---

## ✅ **O QUE FOI ATUALIZADO NO README**

| Item | Antes | Depois |
|------|-------|--------|
| **Versão** | 4.2 | 4.3 |
| **Badges** | 7 badges | 8 badges (+ mobile-friendly) |
| **Funcionalidades** | Lista básica | Lista completa com ícones e detalhes |
| **Consulta** | Sem detalhes | Explicação do filtro por capítulo corrigido |
| **Mobile** | Não mencionado | Seção exclusiva "Mobile-Friendly" |
| **Estatísticas** | Básicas | Completas |
| **Links úteis** | 3 links | 4 links (+ SEFAZ/RS) |
| **Seção Mobile** | ❌ Não existia | ✅ Adicionada no final |

---
