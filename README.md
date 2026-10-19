# Segmentação de massas em regiões de interesse de mamografias

Projeto de Trabalho de Conclusão de Curso (TCC) sobre segmentação de massas em regiões de interesse (ROI) de mamografias, utilizando a base CBIS-DDSM.

## Objetivo

Treinar e avaliar um modelo de segmentação para delimitar massas mamárias em recortes de mamografias. O recorte é definido a partir da anotação da lesão, com escala de ROI igual a 2,0.

## Base de dados

O projeto utiliza a base **CBIS-DDSM**. As imagens e máscaras não estão incluídas neste repositório. Consulte os termos de acesso e uso da base antes de utilizá-la.

## Resultados

No conjunto de teste, o resumo salvo registra 181 imagens de 99 pacientes, com limiar de 0,8:

| Métrica | Resultado |
|---|---:|
| Dice macro (média ± desvio-padrão) | 0,9071 ± 0,0594 |
| Dice macro (mediana) | 0,9213 |
| Dice micro | 0,9125 |
| IoU médio | 0,8346 |
| Precisão média | 0,9027 |
| Sensibilidade média | 0,9183 |
| Especificidade média | 0,9849 |

Os resultados descrevem a execução registrada nos arquivos do projeto. Eles não substituem uma avaliação clínica.

## Estrutura dos resultados

- `resultados_roi_massas/modelos/`: pesos dos modelos treinados.
- `resultados_roi_massas/metricas_e_dados/`: métricas, histórico e arquivos auxiliares em CSV/JSON.
- `resultados_roi_massas/graficos/`: gráficos e imagens de resultados.
- `resultados_roi_massas/graficos_tcc/`: figuras e tabela preparadas para o TCC.
- `resultados_roi_massas/predicoes_roi_teste/`: predições geradas para imagens de teste.

## Execução

O notebook principal está disponível neste repositório. Para executá-lo, configure os caminhos para as imagens e máscaras da base CBIS-DDSM no seu ambiente. O notebook foi preparado para Google Colab e pode exigir montagem do Google Drive.

## Requisitos

As dependências utilizadas devem ser conferidas nas células de instalação/importação do notebook.

## Observação

Este projeto tem finalidade acadêmica e de pesquisa. Não deve ser utilizado para diagnóstico médico.
