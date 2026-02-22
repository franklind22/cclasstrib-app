
# 🧾 **cClassTrib por NCM - Reforma Tributária 2026**

## 📱 **APP WEB DE ALTA PERFORMANCE - LC 214/2025**

**Consulta cClassTrib por NCM** com carregamento assíncrono e arquitetura desacoplada. Sistema otimizado para a Reforma Tributária IBS/CBS oficial do governo brasileiro.

### ✨ **🚀 DEMO AO VIVO**

🔗 https://franklind22.github.io/cclasstrib/
📱 Teste: 01012100 → Enter → ✅ Cavalos Reprodutores (Cesta Básica)

## 🎯 **NOVIDADES DA VERSÃO 3.0 (ARQUITETURA DE DADOS)**

| Feature | Status | Descrição |
|---------|--------|-----------|
| 🗄️ **Arquitetura JSON** | ✅ **ATIVO** | Banco de dados externo em `dados.json` |
| 🚀 **Escalabilidade** | ✅ **ALTA** | Suporte para **5.000+ NCMs** sem perda de performance |
| ⚡ **Fetch API** | ✅ **ATIVO** | Carregamento assíncrono via JavaScript Moderno |
| 🔍 **Busca Híbrida** | ✅ **OK** | Busca por NCM específico ou filtros por Anexo/CST |

## 🎨 **VISUAL E INTERFACE**

Header: Gradiente moderno azul-roxo responsivo
Botões: Cores semânticas (Verde=Busca, Cinza=Limpar, Laranja=Exportar)
Tabela: Sticky header com scroll interno e paginação inteligente
Mobile-First: Otimizado para visualização em Android e iOS

## 💾 **BASE DE DADOS EXPANDIDA (ANEXOS LC 214/2025)**

O app agora carrega dinamicamente todos os capítulos mapeados da Reforma:
- **Anexo I (Cesta Básica):** Carnes, Peixes, Leites, Arroz, Feijão, Óleos (Redução 100%)
- **Anexo VII/VIII (Higiene):** Absorventes, Fraldas, Sabonetes e Dentifrícios
- **Anexo XV (Hortifrúti):** Ovos, Frutas, Legumes e Hortaliças (Redução 100%)
- **Capítulos 01 a 25:** Cobertura completa de proteínas, cereais e minerais básicos.

## 🚀 **COMO ATUALIZAR OS DADOS**
Com a nova estrutura, o desenvolvimento ficou mais fácil:
1. **Não altere o `index.html`** para adicionar produtos.
2. Edite apenas o arquivo **`dados.json`**.
3. Adicione o novo NCM e seus atributos. O site reflete a mudança instantaneamente após o commit.

## ⚙️ **TECNOLOGIAS**

HTML5 | CSS3 (Grid/Flexbox) | Vanilla JS (ES6+)
Fetch API (Async/Await) | JSON dinâmico externo
Trie O(1) Search | LocalStorage Cache (Histórico)
Performance: Carregamento de base robusta em < 100ms

## 📊 **ESTATÍSTICAS**

NCMs Mapeados: 300+ (em expansão contínua)
Tempo de Busca: ~2ms (O(1) search)
Paginação: 20 itens por página
Tamanho do Arquivo: ~18KB (Interface) + JSON de Dados

## 🎉 **ATUALIZAÇÕES RECENTES (22/02/2026)**

✅ Migração completa para Banco de Dados Externo (dados.json)
✅ Removido limite de 60 NCMs (Base agora ilimitada)
✅ Implementado Estado de Carregamento (Loading) para conexões móveis
✅ Correção de filtros globais para funcionar com dados assíncronos

**⭐ Star se ajudou!** **💡 NCM faltando?** Basta editar o `dados.json` ou abrir uma issue.  
**👨‍💻 Dev:** Franklin D22 - 2026
