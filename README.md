# 📈 Monitor de Preços Marketplace (Shopee & Mercado Livre)

Este projeto é uma ferramenta em Python desenvolvida para ser executada via **Google Colab**. O objetivo é monitorar anúncios de "grandes players" e concorrentes em marketplaces, capturando preços e variações para sugerir ajustes estratégicos em tempo real.

## 🚀 Objetivo Estratégico
Como representante comercial, o tempo de reação a uma baixa de preço do concorrente é crítico. Este script automatiza a varredura das páginas públicas, permitindo:
*   **Identificar quedas de preço** antes que elas afetem suas vendas.
*   **Calcular margens de segurança** baseadas no seu preço de custo.
*   **Diferenciar estratégias** entre anúncios simples e anúncios com variações.

## 🛠️ Funcionalidades
- **Scraping Robusto:** Utiliza extração de dados via `JSON Preloaded State` e `Meta Tags`, tornando-o mais resistente a mudanças de layout dos sites.
- **Suporte Multi-Plataforma:** Monitora links do Mercado Livre e Shopee simultaneamente.
- **Análise de Variações:** Capaz de identificar preços distintos dentro do mesmo anúncio (quando disponíveis no código-fonte público).
- **Relatório Comparativo:** Gera uma tabela (DataFrame) com o status da ação (ex: 🚨 BAIXAR ou ✅ COMPETITIVO).

## 📋 Como Usar

1.  **Acesse o Google Colab:** [colab.research.google.com](https://colab.research.google.com/)
2.  **Crie um Novo Notebook:** E cole o código disponível no arquivo `monitor.py` deste repositório.
3.  **Configure seus Produtos:** No bloco de configuração do script, adicione os links e seus custos:
    ```python
    meus_produtos = [
        {"nome": "Seu Produto", "url": "URL_DO_CONCORRENTE", "meu_custo": 50.00}
    ]
    ```
4.  **Execute:** Clique em "Play" e aguarde a geração do relatório.

## ⚠️ Considerações Técnicas
*   **Limites de Acesso:** Marketplaces possuem sistemas anti-bot. Recomenda-se um intervalo (`time.sleep`) entre as consultas para evitar bloqueios de IP.
*   **Páginas Públicas:** O script lê apenas informações disponíveis para qualquer comprador, respeitando os termos de uso de visualização pública.
*   **Manutenção:** Caso o marketplace altere radicalmente a estrutura da página, os seletores de classe CSS ou os caminhos JSON podem precisar de atualização.

## ⚖️ Licença
Este projeto é para fins de estudo e automação comercial privada. Certifique-se de utilizar de forma ética e em conformidade com as diretrizes das plataformas monitoradas.

---
*Desenvolvido para otimização de operações de distribuição e vendas.*
