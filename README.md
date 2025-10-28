# grafana-stylish
Este script JavaScript é uma configuração customizada para o painel Business Charts (Volkov Labs), utilizando a extensão ECharts Liquid Fill. Ele transforma uma única métrica percentual ($0-100\%$) em uma visualização de status altamente dinâmica e estilizada.

O código é projetado para ser inserido na área de configuração customizada do painel Business Charts do Grafana, aproveitando sua capacidade de renderizar opções ECharts avançadas.

Utiliza shape: 'container' para que o medidor preencha 100% da área do painel, criando um formato retangular ideal para dashboards de negócios e visões de SLA.

Gera quatro camadas de ondas com cores progressivamente mais claras (usando selectedPalette), criando um efeito visual de profundidade e movimento mais complexo.

O estilo da visualização (cor das ondas, contorno e fundo) é automaticamente definido por faixas de valor:
Azul (Padrão/Ótimo): Valores Menores ou iguais a  40
Laranja (Atenção/Intermediário): Valores entre 41 - 70
Vermelho (Crítico/Alerta): Valores acima de 71

O valor percentual é exibido duas vezes: em preto na área não preenchida (textStyle) e em branco com sombra na área preenchida (insideText), garantindo contraste e clareza contra qualquer cor de onda.

Após a configuração padrão do grafana e adicionar o Bussiness Char, apenas copie o código e cole na opção Funcion.

