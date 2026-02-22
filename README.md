# 🧾 **cClassTrib por NCM - Reforma Tributária 2026**

## 📱 **APP WEB DE ALTA PERFORMANCE - LC 214/2025**

**Consulta de cClassTrib por NCM** com arquitetura de dados desacoplada. Este sistema foi recalibrado para a **Reforma Tributária IBS/CBS**, oferecendo uma base de referência precisa para a transição tributária brasileira.

### ✨ **🚀 DEMO AO VIVO**
🔗 [https://franklind22.github.io/cclasstrib/](https://franklind22.github.io/cclasstrib/)

---

## 🎯 **NOVIDADES DA VERSÃO 4.0 (AUDITORIA E INTEGRIDADE)**

Diferente das versões anteriores, a V4.0 focou na **higienização e precisão técnica**. Removemos classificações genéricas e corrigimos distorções de alíquotas presentes em versões legadas.

| Feature | Status | Descrição Técnica |
|---------|--------|-------------------|
| 🗄️ **Arquitetura JSON** | ✅ **ATIVO** | Separação total entre lógica de UI (`script.js`) e dados (`dados.json`). |
| ⚖️ **Fidelidade Legal** | ✅ **OK** | Mapeamento direto dos Anexos I, VII, VIII, IX e XV da LC 214/2025. |
| 🔍 **Nomenclatura TIPI** | ✅ **ATIVO** | Descrições atualizadas conforme a Tabela de Incidência de IPI oficial. |
| 🛡️ **Sanidade de Dados** | ✅ **OK** | Correção de NCMs de construção e eletrónicos (movidos para Alíquota Integral). |
| ⚡ **Performance O(1)** | ✅ **ATIVO** | Busca indexada por chave de objeto, garantindo resposta instantânea. |

---

## ❓ **POR QUE A BASE DE NCMS FOI REDUZIDA?**

A redução no volume de NCMs nesta atualização não é uma perda de conteúdo, mas um **ganho de confiabilidade**. O ficheiro anterior continha "ruído" que poderia induzir a erros fiscais.

1. **Eliminação de Falsos Positivos:** Itens como **Aço (Cap. 72)**, **Cimento (NCM 2523)** e **Eletrónicos (Cap. 85)** estavam incorretamente marcados com 100% de redução. Agora, seguem corretamente a **Regra Geral (CST 000)**.
2. **Fim das Descrições Genéricas:** Substituímos o texto padrão *"Vendas de produtos destinados à alimentação..."* por nomes reais (ex: "Arroz polido", "Carne Bovina", "Smartphone").
3. **Foco nos Regimes Especiais:** Priorizámos os NCMs que realmente possuem **Redução (60% ou 100%)** ou **Imunidade**, facilitando a consulta de itens que saem da alíquota padrão.

---

## 📊 **MAPEAMENTO DA LEGISLAÇÃO (LC 214/2025)**

O motor de consulta e o `dados.json` validam os seguintes cenários da nova lei:

### **1. Redução de 100% (Cesta Básica & Saúde)**
* **Anexo I:** Carnes, Peixes, Leites, Arroz, Feijão, Farinhas, Açúcar e Óleos.
* **Anexo VII:** Medicamentos de uso humano e produtos de cuidados básicos (CST 200).

### **2. Redução de 60% (Higiene e Insumos Agro)**
* **Anexo VIII:** Sabonetes, cremes dentais, papéis higiénicos e higiene pessoal.
* **Anexo IX:** Rações para animais de produção, sementes e fertilizantes (Insumos Agro).

### **3. Imunidade Objetiva (Hortifrúti e Cultura)**
* **Anexo XV:** Frutas frescas, legumes, hortaliças e ovos (**CST 410**).
* **Art. 150 CF:** Livros, jornais e papel destinado à sua impressão.

---

## ⚙️ **DETALHES TÉCNICOS E PERFORMANCE**

### **Interface e UX**
* **Design Mobile-First:** Tabelas responsivas com `sticky header` para facilitar a leitura.
* **Cores Semânticas:** Diferenciação visual entre itens com Redução (Verde) e Integral (Cinza).
* **LocalStorage Cache:** O sistema armazena o teu histórico das últimas 10 pesquisas localmente.

### **Estatísticas de Performance**
* **Tempo de Busca:** ~2ms (O(1) search).
* **Carregamento Inicial:** < 100ms para a base robusta de dados.
* **Paginação:** Renderização inteligente de 20 itens por página para poupar memória do dispositivo.

---

## 🚀 **COMO ATUALIZAR OS DADOS**

Para expandir o banco de dados sem quebrar a lógica do sistema, siga este padrão no `dados.json`:

```json
"CÓDIGO_NCM": [
  {
    "cclasstrib": "200003", 
    "cst": "200",          // 000 (Integral), 200 (Reduzido), 410 (Imune)
    "descricao": "NOME REAL DO PRODUTO CONFORME TIPI",
    "pReducao": "100%",    // 0%, 60% ou 100%
    "legislacao": "LC 214/2025 Anexo X",
    "regime": "reducao",   // integral, reducao ou imunidade
    "ativo": true
  }
]


⚠️ AVISO LEGAL: Este software é uma ferramenta de simulação pedagógica e de apoio ao desenvolvimento. Os dados devem ser validados por um profissional de contabilidade antes de serem aplicados em ambientes de produção fiscal.


**⭐ Star se ajudou!** **💡 NCM faltando?** Basta editar o `dados.json` ou abrir uma issue.  
**👨‍💻 Dev:** Franklin D22 - 2026
