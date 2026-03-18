
<div align="center">
  <img src="https://img.icons8.com/fluency/96/000000/search.png" width="80" height="80"/>
  <h1>🧾 cClassTrib · Consulta NCM</h1>
  <p><strong>Reforma Tributária IBS/CBS · LC 214/2025</strong></p>
  
  <!-- BADGES FODAS -->
  <p>
    <img src="https://img.shields.io/badge/versão-4.0-blue?style=for-the-badge&logo=github" alt="Versão">
    <img src="https://img.shields.io/badge/NCMs-750%2B-green?style=for-the-badge&logo=files" alt="NCMs">
    <img src="https://img.shields.io/badge/CSTs-154-orange?style=for-the-badge&logo=tags" alt="CSTs">
    <img src="https://img.shields.io/badge/licença-MIT-red?style=for-the-badge&logo=opensource" alt="Licença">
    <img src="https://img.shields.io/badge/status-em%20produção-success?style=for-the-badge&logo=vercel" alt="Status">
  </p>

  <!-- LINK DEMO -->
  <h3>
    <a href="https://franklind22.github.io/cclasstrib-app/">
      🚀 ACESSE A DEMO AO VIVO
    </a>
  </h3>
  
  <!-- SCREENSHOT (opcional - adicione depois) -->
  <!-- <img src="assets/screenshot.png" width="800" alt="Screenshot do App"> -->
</div>

---

## 📋 **SOBRE O PROJETO**

**cClassTrib** é uma ferramenta de consulta da classificação tributária IBS/CBS por código NCM, baseada na **Lei Complementar 214/2025** — a Reforma Tributária do governo brasileiro.

Desenvolvido para **contadores, profissionais fiscais e empresários**, o sistema oferece:

✅ **Consulta rápida** de NCMs com redução/imunidade  
✅ **Lista completa de CSTs** com documentos fiscais  
✅ **Navegação por capítulos** da NCM  
✅ **Informações oficiais** da LC 214/2025  
✅ **Design moderno e responsivo** (funciona em qualquer tela)

---

## ✨ **FUNCIONALIDADES**

### 🔍 **ABA CONSULTA**
| Funcionalidade | Descrição |
|----------------|-----------|
| **Pesquisa por NCM** | Busca por código de 4, 6 ou 8 dígitos |
| **Busca por capítulo** | Seletor de capítulos NCM |
| **Exemplos rápidos** | Clique para testar |
| **Filtros** | Por CST 200, 410, redução, imunidade |
| **Histórico** | Últimas consultas salvas localmente |
| **Exportação** | Download dos resultados em JSON |

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
| **Filtros por grupo** | CST 200, 410 e outros |
| **Pesquisa** | Por CST, cClassTrib ou descrição |
| **Documentos fiscais** | DFes relacionados a cada CST |
| **Paginação** | 20 itens por página |
| **Exportação** | Download da lista completa |

### ℹ️ **ABA SOBRE**
| Funcionalidade | Descrição |
|----------------|-----------|
| **Estatísticas** | NCMs, regras, versão |
| **Legislação** | Mapeamento dos anexos da LC 214/2025 |
| **Links úteis** | Acesso direto às fontes oficiais |
| **Aviso legal** | Informações importantes |

---

## 📊 **ESTATÍSTICAS DA BASE**

| Item | Quantidade |
|------|------------|
| **NCMs mapeados** | 750+ |
| **CSTs documentados** | 154 |
| **Anexos da LC 214** | 11 |
| **Documentos fiscais** | 15 tipos diferentes |

---

## 🎨 **TECNOLOGIAS UTILIZADAS**

<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Pages-222222?style=for-the-badge&logo=githubpages&logoColor=white" />
  <img src="https://img.shields.io/badge/Font%20Awesome-528DD7?style=for-the-badge&logo=fontawesome&logoColor=white" />
</div>

---

## 📁 **ESTRUTURA DO PROJETO**

```
cclasstrib-app/
├── 📄 index.html          # Aplicação principal
├── 📄 dados.json          # Base de dados dos NCMs
├── 📄 README.md           # Documentação (você está aqui)
└── 📁 assets/             # (opcional) Imagens e ícones
```

---

## 🚀 **COMO EXECUTAR LOCALMENTE**

1. **Clone o repositório**
   ```bash
   git clone https://github.com/franklind22/cclasstrib-app.git
   cd cclasstrib-app
   ```

2. **Abra o arquivo**
   - Dê duplo clique no `index.html` ou
   - Use um servidor local:
     ```bash
     npx http-server
     ```

3. **Pronto!** Acesse `http://localhost:8080`

---

## 📖 **COMO ATUALIZAR OS DADOS**

### Para adicionar um novo NCM:
```json
"02013000": [
  {
    "cclasstrib": "200003",
    "cst": "200",
    "descricao": "Carnes de bovino, frescas ou refrigeradas, desossadas",
    "pReducao": "100%",
    "legislacao": "LC 214/2025 Anexo I",
    "regime": "reducao",
    "ativo": true
  }
]
```

### Para adicionar um novo CST:
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

<div align="center">
  <blockquote>
    <p>⚠️ <strong>Este software é uma ferramenta de simulação pedagógica e de apoio ao desenvolvimento.</strong></p>
    <p>Os dados devem ser validados por um profissional de contabilidade antes de serem aplicados em ambientes de produção fiscal.</p>
  </blockquote>
</div>

---

## 👨‍💻 **DESENVOLVEDOR**

<div align="center">
  <img src="https://img.icons8.com/fluency/96/000000/user-male-circle.png" width="80" height="80"/>
  <h3>Franklin D22</h3>
  <p>
    <a href="https://github.com/franklind22">
      <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />
    </a>
    <a href="#">
      <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
    </a>
    <a href="#">
      <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
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

<div align="center">
  <h3>Feito com ❤️ para a comunidade fiscal brasileira</h3>
  <p>© 2026 · Reforma Tributária</p>
  <p>
    <img src="https://img.icons8.com/color/48/000000/brazil.png" width="30"/>
  </p>
</div>
```
