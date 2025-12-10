# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 10/12/2025

Empresa: Abstergo Industries

Responsável: Eric Hiroshi

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Eric Hiroshi. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.
Descrição do Projeto


## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

Etapa 1:
- Nome da ferramenta: AWS Cost Explorer
- Foco da ferramenta: Monitoramento e análise de gastos
- Descrição de caso de uso:
Ferramenta usada para visualizar onde a empresa está gastando mais na nuvem. Permite identificar desperdícios, como servidores ociosos, volumes de armazenamento não utilizados e picos inesperados de consumo. A partir dos relatórios, é possível realizar cortes diretos nos recursos que não estão sendo usados.

Etapa 2:
- Nome da ferramenta: AWS S3 + S3 Lifecycle Policies
- Foco da ferramenta: Armazenamento de baixo custo
- Descrição de caso de uso:
Migração de arquivos, notas, relatórios financeiros e backups para o S3, substituindo armazenamento local caro e instâncias EC2 subutilizadas. Com o uso de Lifecycle Policies, arquivos antigos passam automaticamente para camadas mais baratas, reduzindo gasto contínuo com armazenamento.

Etapa 3:
- Nome da ferramenta: AWS Auto Scaling
- Foco da ferramenta: Ajuste automático de servidores conforme demanda
- Descrição de caso de uso:
Substitir servidores ligados 24h por um grupo de instâncias que aumentam ou diminuem automaticamente de acordo com o volume de pedidos e acessos do sistema. Quando a demanda cai, as máquinas desligam sozinhas, evitando pagamento por capacidade não utilizada.

## Conclusão
A implementação de ferramentas na empresa Abstergo Industries tem como esperado permitir a identificação de desperdícios, redução automática de infraestrutura e armazenamento mais econômico, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

- Capturas de tela dos relatórios de gastos
- Planilha com comparação de custos antes/depois
- Guia de políticas de ciclo de vida do S3

Assinatura do Responsável pelo Projeto:

Eric Hiroshi