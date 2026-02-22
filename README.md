# 🧾 **cClassTrib por NCM - Reforma Tributária 2026**

## 📱 **APP WEB DE ALTA PERFORMANCE - LC 214/2025**

**Consulta cClassTrib por NCM** com carregamento assíncrono e arquitetura desacoplada. Sistema otimizado para a Reforma Tributária IBS/CBS oficial do governo brasileiro.

### ✨ **🚀 DEMO AO VIVO**

🔗 [https://franklind22.github.io/cclasstrib/](https://franklind22.github.io/cclasstrib/)

---

## 🎯 **NOVIDADES DA VERSÃO 4.0 (AUDITORIA E INTEGRIDADE)**

| Feature | Status | Descrição |
|---------|--------|-----------|
| 🗄️ **Arquitetura JSON** | ✅ **ATIVO** | Banco de dados externo em `dados.json` |
| ⚖️ **Fidelidade Legal** | ✅ **OK** | Ajuste rigoroso aos Anexos I, VII, VIII, IX e XV da LC 214/2025 |
| 🛡️ **Sanidade de Dados** | ✅ **OK** | Remoção de inconsistências e correção de NCMs (Construção/Eletrônicos) |
| ⚡ **Fetch API** | ✅ **ATIVO** | Carregamento assíncrono via JavaScript Moderno |

---

## ❓ **POR QUE A BASE DE NCMS FOI REDUZIDA?**

A redução no volume de NCMs nesta atualização é estratégica para garantir a **confiabilidade** do simulador:

1. **Correção de Falsos Positivos:** Itens como Aço, Cimento e Eletrônicos estavam incorretamente marcados como "Cesta Básica". Agora seguem a **Regra Geral (CST 000)**.
2. **Descrições Reais:** Substituímos textos genéricos por nomes oficiais da tabela TIPI/NCM.
3. **Foco em Regimes Especiais:** Priorizamos itens com **Redução (60% ou 100%)** ou **Imunidade**, que são o foco das dúvidas fiscais.

---

## 📊 **MAPEAMENTO DA LEGISLAÇÃO (LC 214/2025)**

- **Anexo I (Cesta Básica):** Redução 100% (Proteínas, Arroz, Feijão, etc.)
- **Anexo VII/VIII (Saúde e Higiene):** Medicamentos (100%) e Higiene Pessoal (60%)
- **Anexo IX (Insumos Agro):** Rações, Sementes e Fertilizantes (60%)
- **Anexo XV (Hortifrúti):** Imunidade - CST 410 (Frutas, Ovos e Legumes)

---

## 🚀 **COMO ATUALIZAR OS DADOS**

Para expandir o banco de dados, adicione novos itens no arquivo `dados.json` seguindo este padrão:

```json
"CÓDIGO_NCM": [
  {
    "cclasstrib": "200003", 
    "cst": "200",          
    "descricao": "NOME REAL DO PRODUTO CONFORME TIPI",
    "pReducao": "100%",    
    "legislacao": "LC 214/2025 Anexo X",
    "regime": "reducao",   
    "ativo": true
  }
]
```
---
##
⚠️ AVISO LEGAL: Este software é uma ferramenta de simulação pedagógica e de apoio ao desenvolvimento. Os dados devem ser validados por um profissional de contabilidade antes de serem aplicados em ambientes de produção fiscal.

⭐ Star se ajudou! 💡 NCM faltando? Basta editar o dados.json ou abrir uma issue.
👨‍💻 Dev: Franklin D22 - 2026
