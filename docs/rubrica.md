# Rubrica

Esta pagina cruza a entrega com os requisitos das paginas de Project, Exchange API, Jenkins, MiniKube, Bottlenecks e Presentation.

## Status geral

| Area | Status | Observacao |
| --- | --- | --- |
| Repositorio individual | Feito | Publicado em GitHub Pages |
| MkDocs individual | Feito | `mkdocs build --strict` passou localmente e site esta publicado |
| Exchange API | Feito | Codigo fonte, testes, Dockerfile, Jenkinsfile e Kubernetes incluidos |
| Jenkins | Parcial | Jenkinsfiles existem nos repos, mas falta evidencia do pipeline executando deploy no EKS |
| MiniKube/Kubernetes | Parcial | Manifests existem, mas falta evidencia em video/print de todos os servicos saudaveis no mesmo cluster |
| Project AWS/EKS | Parcial | A infraestrutura e compartilhada pelo grupo; custo AWS observado foi registrado, mas faltam prints finais de cluster/deploy |
| Load Testing/HPA | Parcial | O teste e do projeto em grupo; falta anexar video do HPA escalando |
| Costs & PaaS | Parcial | Custo real AWS foi registrado; falta estimativa final da AWS Pricing Calculator e descricao concreta do PaaS usado |
| Bottlenecks | Feito | Dois bottlenecks individuais documentados: dependencia externa e observabilidade |
| Apresentacao e video | Pendente | Falta inserir links finais |
| Uso de IA | Documentado | Ver [Uso de IA](uso-ia.md) |

## Fontes da rubrica

- Project Overview: <https://insper.github.io/platform/2026.1/exercises/project/>
- Project AWS: <https://insper.github.io/platform/2026.1/exercises/project/aws/>
- Project EKS: <https://insper.github.io/platform/2026.1/exercises/project/eks/>
- Project CI/CD: <https://insper.github.io/platform/2026.1/exercises/project/ci-cd/>
- Project Load Testing: <https://insper.github.io/platform/2026.1/exercises/project/load-testing/>
- Project Costs & PaaS: <https://insper.github.io/platform/2026.1/exercises/project/costs/>
- Project Presentation: <https://insper.github.io/platform/2026.1/exercises/project/presentation/>
- Exchange API: <https://insper.github.io/platform/2026.1/exercises/exchange/>
- Jenkins: <https://insper.github.io/platform/2026.1/exercises/jenkins/>
- MiniKube: <https://insper.github.io/platform/2026.1/exercises/minikube/>
- Bottlenecks: <https://insper.github.io/platform/2026.1/exercises/bottlenecks/>

## Riscos para 100%

- O enunciado do projeto menciona que o projeto principal deve incorporar as implementacoes individuais como submodules. O repositorio de grupo referencia repos separados, mas neste clone nao ha `.gitmodules`.
- A documentacao do grupo ainda precisa anexar prints finais de EKS, Jenkins, HPA e a estimativa formal da AWS Pricing Calculator.
- A pagina de Presentation pede apresentacao e video. Esta entrega individual ja tem uma pagina para isso, mas os links finais ainda precisam ser inseridos.

## Interpretacao para a entrega individual

Nao e necessario criar uma AWS separada para cada aluno. A infraestrutura AWS/EKS e uma entrega do projeto em grupo. O repositorio individual deve documentar a participacao do aluno, apontar para o projeto completo e incluir os links/evidencias compartilhados.
