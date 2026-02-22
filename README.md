
🧾 cClassTrib por NCM - Reforma Tributária 2026
📱 APP WEB DE ALTA PERFORMANCE - LC 214/2025
Consulta cClassTrib por NCM com carregamento assíncrono e arquitetura desacoplada. Sistema otimizado para a Reforma Tributária IBS/CBS oficial do governo brasileiro.
✨ 🚀 DEMO AO VIVO
🔗 https://franklind22.github.io/cclasstrib/
🎯 NOVIDADES DA VERSÃO 4.0 (AUDITORIA E INTEGRIDADE)
| Feature | Status | Descrição |
|---|---|---|
| 🗄️ Arquitetura JSON | ✅ ATIVO | Banco de dados externo em dados.json |
| ⚖️ Fidelidade Legal | ✅ OK | Ajuste rigoroso aos Anexos I, VII, VIII, IX e XV da LC 214/2025 |
| 🛡️ Sanidade de Dados | ✅ OK | Remoção de inconsistências e correção de NCMs (Construção/Eletrônicos) |
| ⚡ Fetch API | ✅ ATIVO | Carregamento assíncrono via JavaScript Moderno |
📊 MAPEAMENTO DA LEGISLAÇÃO (LC 214/2025)
 * Anexo I (Cesta Básica): Redução 100% (Proteínas, Arroz, Feijão, etc.)
 * Anexo VIII/IX (Higiene/Agro): Redução 60% (Sabonetes, Rações, Fertilizantes)
 * Anexo XV (Hortifrúti): Imunidade - CST 410 (Frutas, Ovos e Legumes)
🚀 COMO ATUALIZAR OS DADOS
Para expandir o banco de dados, siga este padrão no arquivo dados.json:
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

⚠️ AVISO LEGAL: Este software é uma ferramenta de simulação pedagógica e de apoio ao desenvolvimento. Os dados devem ser validados por um profissional de contabilidade antes de serem aplicados em ambientes de produção fiscal.
⭐ Star se ajudou! 💡 NCM faltando? Basta editar o dados.json ou abrir uma issue.
👨‍💻 Dev: Franklin D22 - 2026
Por que agora vai funcionar?
 * Eu fechei o bloco de código do JSON com as três crases.
 * Coloquei uma linha separadora (---).
 * O Aviso Legal está solto no final do arquivo, sem nenhuma crase depois dele. No GitHub, ele vai aparecer como texto comum em negrito, exatamente como você quer.
