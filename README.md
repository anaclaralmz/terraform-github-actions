# Automate Terraform with GitHub Actions

This repo is a companion repo to the [Automate Terraform with GitHub Actions tutorial](https://developer.hashicorp.com/terraform/tutorials/automation/github-actions).
# Tecnologias
- **Terraform:** É uma ferramenta de infraestrutura como código (IaC) que permite definir e provisionar recursos de infraestrutura de forma declarativa;
- **Github Actions:** É um serviço de automação integrado ao GitHub, que permite automatizar fluxos de trabalho dentro de repositórios;
- **AWS:** fizemos o deploy automatizado do repositório em uma instância EC2 da AWS (Amazon Web Services)
# Conceitos aprendidos
## Infra as code (IaC)
- É o conceito de gerenciar e provisionar recursos de infraestrutura usando código. 
- Isso traz vantagens como:
  -  controle de versão
  -  reprodutibilidade
  -  automação -> ao integrarmos o Terraform ao Github actions, foi possivel acionar um script especifico quando um PR é criado e mergiado, para que o repositório seja deployado em uma instância EC2, de forma automatizada.
- O Terraform é uma das ferramentas populares para implementar IaC, e oferece esse recurso de forma simples e rápida.
## Processo de automação do deploy
![imagem1](/assets/d.png)
1. Criar a conta no Terraform, e uma organização com um workflow;
2. Rodar o learner lab na AWS academy;
3. Registrar as credenciais da AWS no workflow do terraform;
![imagem1](/assets/e.png)
5. Configurar os arquivos .yml da aplicação com as informações do workflow criado, e com a região certa da AWS;
6. Criar um Pull Request no repositório, que vai acionar o script criado:
![imagem1](/assets/g.png)
7. Dar merge no PR, e acompanhar a execução do script de automação:
![imagem1](/assets/a.png)
![imagem1](/assets/c.png)
8. Quando a instância for criada com sucesso, aparecerá uma url que direciona para seu endereço na web
![imagem1](/assets/f.png)
![imagem1](/assets/b.png)
9. Por fim, dentro do console da AWS, podemos ver que a instância, de fato, foi criada!
![imagem1](/assets/h.png)
