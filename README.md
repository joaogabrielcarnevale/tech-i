# Aplicação Web

## Como realizar manualmente o build e deployment deste projeto

Inicie uma instância EC2 utilizando o `Amazon Linux`;

Em sua instância, instale o `git` utilizando o seguinte comando:

    sudo yum -y install git

Siga as instruções do link a seguir para instalar o node em sua instancia:

    https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/setting-up-node-on-ec2-instance.html

Realize o clone deste repositório através do seguinte comando:

    git clone https://github.com/bemer/tech-u.git

Acesse o diretório `tech-u` recém criado através do comando:

    cd tech-u

Dentro do diretório tech-u execute o seguinte comando para instalar o módulos necessários para a aplicação node:

    npm install

Agora, instale o `gulp` através do seguinte comando:

    npm install --global gulp

Execute o gulp:

    gulp

Instale o `nginx`:

    sudo amazon-linux-extras install -y nginx1.12

Copie o diretório com sua aplicação para o diretório `html` do nginx utilizando:

    sudo cp -rf ~/tech-u /usr/share/nginx/html/

Inicie o nginx:

    sudo service nginx start

Acesse a sua aplicação através da url:

    <Hostname de sua instancia EC2>


## Realizei o deployment. E agora?

Pode ser que você não tenha conseguido acessar sua aplicação devidamente. Não se preocupe. Isso faz parte do exercício. Agora, seu objetivo é corrigir eventuais problemas, conseguir acessar sua aplicação e automatizar este processo de deployment utilizando as ferramentas existentes no ecossistema da AWS (AWS CloudFormation, awscli).

No final desta sprint, seu grupo precisará realizar uma apresentação com 3 slides contendo:

* Desenho da arquitetura;
* O que deu certo;
* O que deu errado durante o processo (lições aprendidas).

Além dos scripts com o processo de automação.
