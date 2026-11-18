# Processos ITIL no Bizagi — Incidentes, Problemas e Requisições

Modelagem BPMN, feita no Bizagi Modeler, dos processos de **Gerenciamento de Incidentes**, **Gerenciamento de Problemas** e **Gerenciamento de Requisições de Serviço**, seguindo as práticas da ITIL.

Raias: **Cliente → Analista N1 (Service Desk) → Analista N2 → Desenvolvimento**, mais a raia **Projetos** no processo de Requisições.

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `ITIL_Incidentes_Problemas_Requisicoes.bpm` | Modelo completo, com os 3 diagramas em abas |
| `separados/` | Cada processo em um `.bpm` próprio |
| `previa/` | Imagens dos diagramas |

Para abrir: instale o [Bizagi Modeler](https://www.bizagi.com/pt/plataforma/modeler) (gratuito) e abra o arquivo `.bpm`. Cada tarefa tem uma descrição com a orientação ITIL, visível nas propriedades do elemento.

## 1. Gerenciamento de Incidentes

Objetivo: restaurar o serviço o mais rápido possível. O N1 registra, categoriza e prioriza (Impacto x Urgência), trata incidentes graves (P1) e resolve pela Base de Conhecimento. Se não conseguir, escala para o N2, que diagnostica e corrige falhas operacionais ou, quando é bug, reproduz o erro e aciona o Desenvolvimento. O cliente valida a solução, e o N1 decide se é preciso abrir um Problema e encerra o incidente.

![Gerenciamento de Incidentes](previa/1_Incidentes.png)

## 2. Gerenciamento de Problemas

Objetivo: eliminar a causa raiz. O processo começa de forma reativa (incidentes recorrentes ou graves) ou proativa (análise de tendências). Inclui análise de causa raiz, registro de workaround e de Erro Conhecido (KEDB), avaliação de custo x benefício, correção definitiva via mudança (GMUD), validação em produção e lições aprendidas.

![Gerenciamento de Problemas](previa/2_Problemas.png)

## 3. Gerenciamento de Requisições

Objetivo: atender pedidos que não são falhas. A requisição é classificada pelo Catálogo de Serviços e passa por aprovação quando necessário. Depois segue um de três caminhos: **padrão** (N1), **técnica** (N2 e Desenvolvimento) ou **projeto** (requisitos, proposta, desenvolvimento, homologação com o cliente e implantação). O cliente valida, responde a pesquisa de satisfação e o N1 encerra.

![Gerenciamento de Requisições](previa/3_Requisicoes.png)
