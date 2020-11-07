# Projeto This is my Architecture

## Task 1: Deploy da Aplicação Web

### Como realizar manualmente o build e deployment deste projeto

Inicie uma instância EC2 utilizando o `Amazon Linux 2`;

Em sua instância, instale o `git` utilizando o seguinte comando:

    sudo yum -y install git

Realize o clone deste repositório através do seguinte comando:

    git clone https://github.com/joaogabrielcarnevale/tech-i.git

Acesse o diretório `tech-i` recém criado através do comando:

    cd tech-i

Instale o `nginx`:

    sudo amazon-linux-extras install -y nginx1.12

Copie o diretório com sua aplicação para o diretório `html` do nginx utilizando:

    sudo cp -rf ~/tech-u /usr/share/nginx/html/

Inicie o nginx:

    sudo service nginx start

Acesse a sua aplicação através da url:

    <Hostname de sua instancia EC2>

### Realizei o deployment. E agora?

Pode ser que você não tenha conseguido acessar sua aplicação devidamente. Não se preocupe. Isso faz parte do exercício. Agora, seu objetivo é corrigir eventuais problemas e conseguir acessar sua aplicação.

## Task 2: Alta Disponibilidade e Escalabilidade

Nesta etapa defina métricas escalabilidade e deployment Multi-AZ junto ao seu Cohort Leader.

Exemplo: *mínimo de 1 instância em 2 AZs distintas, que escale horizontalmente quando a métrica **CPUUtilization** for maior que 40%.*

### Escalabilidade

Lembrando do conceito de escalabilidade horizontal, aplique esse conceito na sua aplicação utilizando as ferramentas existentes no ecossistema da AWS (Elastic Load Balancing, AWS Auto Scaling). Defina métricas e faça testes de carga verificando que sua aplicacão escala.

Ferramentas de teste de carga: Blazemeter, Jmeter, Locust, Loader.io, Bees With Machine Gun.

### Alta Disponibilidade

Nesta etapa verifique se sua aplicação segue o conceito de deployment Multi-AZ. 

## Task 3: Deploy Automatizado

Automatize o processo de deployment do seu ambiente utilizando as ferramentas existentes no ecossistema da AWS (AWS CloudFormation, awscli).

## Apresentação

Ao final do projeto, seu grupo precisará realizar uma apresentação com 3 slides contendo:

* Desenho da arquitetura;
* O que deu certo;
* O que deu errado durante o processo (lições aprendidas).

Além dos scripts com o processo de automação.
