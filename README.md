# 🌊 Grafana Business Charts: Liquid Fill Gauge Dinâmico (SLA) - Formato ▢

Este é um script JavaScript (opção ECharts) para o painel **Business Charts** (Volkov Labs) do Grafana, que implementa um medidor de preenchimento líquido (`liquidFill`) com cores dinâmicas baseadas em faixas de status (SLA).

Ele transforma uma única métrica percentual (assumida entre 0% e 100%) em uma visualização de status altamente dinâmica e estilizada.

## ✨ Funcionalidades Principais

* **Visualização Retangular de Status:** Utiliza `shape: 'container'` para preencher 100% do painel.
* **Efeito de Profundidade com Ondas:** Gera **quatro camadas de ondas** com cores progressivamente mais claras para um efeito visual de profundidade.
* **Esquema de Cores Dinâmico (SLA):** O estilo (ondas, contorno e fundo) é automaticamente definido por faixas de valor:
    * **Azul (Padrão/Ótimo):** Valores $\le 40$
    * **Laranja (Atenção/Intermediário):** Valores $41 - 70$
    * **Vermelho (Crítico/Alerta):** Valores $\ge 71$
* **Legibilidade Superior:** Rótulo em preto (fora da onda) e branco (dentro da onda) para máximo contraste.

## 🚀 Como Usar no Grafana

1.  **Instale o Plugin:** Certifique-se de ter o plugin **Business Charts** (`volkovlabs-echarts-panel`) instalado no seu Grafana.
2.  **Adicione o Painel:** Adicione um novo painel e selecione o tipo **Business Charts**.
3.  **Configure a Query:** Adicione sua query que retorna o valor percentual (0-100).
4.  **Insira o Código:** Vá para as configurações do painel e cole o conteúdo completo do arquivo `liquidFillGauge.js` (abaixo) na seção de código  (Function) JavaScript/ECharts.
