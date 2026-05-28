# Projeto

## Visao geral

O projeto em grupo e uma plataforma de loja baseada em microservicos.

Servicos:

- `account-service`: contas e credenciais;
- `auth-service`: autenticacao e JWT;
- `gateway-service`: entrada unica da aplicacao;
- `product-service`: cadastro e consulta de produtos;
- `order-service`: criacao e consulta de pedidos;
- `exchange-service`: cotacoes de moeda.

## Contribuicao individual

A contribuicao individual registrada neste repositorio e o `exchange-service`, que foi implementado originalmente dentro da organizacao `insper-aulas` e agora tambem consta neste repositorio individual.

## Infraestrutura AWS/EKS

A infraestrutura AWS/EKS nao foi criada separadamente para este repositorio individual. Ela pertence ao projeto em grupo e e compartilhada pelos servicos da aplicacao.

Neste repositorio individual, a parte avaliada de Raphael fica documentada e versionada como:

- codigo fonte do `exchange-service`;
- Dockerfile do `exchange-service`;
- Jenkinsfile do `exchange-service`;
- manifests Kubernetes do `exchange-service`;
- documentacao individual em MkDocs;
- links para a infraestrutura e para as evidencias do projeto em grupo.

Assim, a entrega individual referencia a AWS/EKS do grupo, enquanto o repositorio individual guarda a contribuicao e a documentacao pessoal exigidas na entrega.

## Documentacao do projeto

- Documentacao publicada do grupo: <https://insper-aulas.github.io/micro_api_26.1/>
- Arquitetura do grupo: <https://insper-aulas.github.io/micro_api_26.1/projeto/arquitetura/>
- Execucao local: <https://insper-aulas.github.io/micro_api_26.1/projeto/execucao-local/>
- Validacao: <https://insper-aulas.github.io/micro_api_26.1/projeto/validacao/>
- AWS: <https://insper-aulas.github.io/micro_api_26.1/infra/aws/>
- EKS: <https://insper-aulas.github.io/micro_api_26.1/infra/eks/>
- CI/CD: <https://insper-aulas.github.io/micro_api_26.1/infra/cicd/>
- Load Testing: <https://insper-aulas.github.io/micro_api_26.1/load-testing/>
- Custos: <https://insper-aulas.github.io/micro_api_26.1/costs/>
- PaaS: <https://insper-aulas.github.io/micro_api_26.1/paas/>

## Codigo fonte do projeto

O codigo fonte completo fica distribuido nos repositorios listados em [Repositorios](repositorios.md).
