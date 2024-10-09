# resumo_lab_5
Desafio de Projeto: Configurando recursos e dimensionamentos em máquinas virtuais na Azure
Resumo Laboratório "Computação e rede": criar uma máquina virtual no Portal Azure
- Configurações pré-definidas de criação: A série F é recomendada para cargas de trabalho otimizadas para a memória, atendendo uma solicitação.
  Validar os modelos de VMs que famílias escolher para cada situação. "More virtual machines and related solutions" -  Modelo de Linus usando WordPress (Scalable WordPress using Azure VM)
  VM com configurações pré-definidas e aplicações prontas. Modelo de teste e desenvolvimento, com um conjunto de recursos (BD, Conjunto de dimensionamento, chaves SSH, etc.), otimizam o trabalho.
Criar 1 VM: Assinatura, Grupo de recurso: Az_900_Lab_Dio, nome: machine01, Região: US East2, opções de disponibilidade: nenhuma redundância (teste, Zona de disponibilidade: Z1
  Tamanho: Standard DS1_v2.
  - Condições de escala: padrão, Contagem de Instância 2 - Conjunto de dimensionamento VM: modo de orquestração flexível (verificar quantas máquinas e crescimento), atualizar manualmente ou por dimensionamento automático (quando necessitar de mais máquinas).
  - Instância em Spot (uso quando disponível com um custo reduzido), uso da carga de trabalho até que seja solicitado o uso da máquina. É uma estratégia interessante para desenvolvimento e teste, mas não para produção. CPU, famílias, mas quando o contexto é de  teste é para usar a  mais barata.
  - Verificar/selecionar o tamanho da VM, para o modelo de trabalho, verificar na tabela qual é a melhor opção modelo (família), otimizada para seu uso.
  - Contas de administrador: usuário e senha, Regras de porta de entrada.
  - Discos: tamanhos de discos (vários modelos premium mais caro). Excluir com VM deixar marcado, para não aumentar os custos (evitar discos órfãos).
  - Rede virtual: Machine01-vnet1. Determinar porta de entrada: somente meu IP. Marcar: excluir o IP público e a NIP quando a VM for excluída.
  - Gerenciamento: AD, desligamento automático. Horário e e-mail. Backup habilitar, nesse caso é uma IaaS, então é necessário. Estude cada caso. Verifique a política.
  - Monitoramento: configurar regras de alertas configuradas. Avançado: Pode selecionar uma extensão para quando a VM estiver subindo. Ex.: HPE Service, ou um app de VM.
  - Tags, Revisar e Criar: verifique a estimativa de custo.
Entender as etapas de criação de VM.
- Explorar a área de trabalho do Azure: Se não criar um pool tem que (criar uma máquina personalizada, que será destinada ao uso exclusivo de alguém, questão do custo)
    - Criar um pool de hosts (pode utilizar os mesmos recursos para 5 pessoas, otimiza custos), trabalha com base no balanceamento de carga em largura e profundidade e o limite máximo de     seção (nº máx. usuários/pool). Selecionar assinatura, grupo de recursos, nome, tipo de grupo de app preferencial: área de trabalho ou remoteapp. Nº de ususários. Add VM (sim, continua a configuração). Tipo de seção: individual e em grupo. Oferece um ambiente personalizada no Azure - na Área de trabalho. Em qual modelo: IaaS, PaaS ou Saas.
  - Aplicativo de funções (Azure Functions) - modelos de automação: pode ser código ou imagem de container. Que linguagem? Java/NET (Windwons) Python (Linux). Com ou sem servidor. Conta de Armazenamento. Versão e Linguagens de programação que estão ligadas nesse cenário.
