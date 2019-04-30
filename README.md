# CreatingInstancesAWS

Primeiro lugar iremos acessar a conta da AWS, e iremos serviços e no menu escolheremos opção EC2, assim que acessar o dashboard do EC2, veremos no lado esquerdo a opção Instances, clicaremos nessa opção, e apresentará todas as Instancias criadas, caso não haja, clique no botão Lauch Instance.
Ao clicar no botão, ele mostrará as imagens que estão disponíveis pela AWS na lista Quick Start, caso já tenha alguma imagem crida, clique em My AMIs.
Iremos criar uma Instancia com uma imagem já predefinida pela Amazon, a imagem escolhida foi Ubuntu Server 18.04 LTS (HVM), SSD Volume Type - ami-0a313d6098716f372, clica em select.
Nesse passo, A AWS mostrará o tipo de maquina que você poderá escolher, iremos selecionar a opção t2.micro, pois é a opção elegivel pelo free tier. Cada opção há um certo poder de processamento, memória, storage, network performace e etc, você deve escolher qual é a melhor opção que se adeque a sua empresa.
No passo 3, são as configurações referentes a configuração da instancia, como número de instancias, VPC, subnet, public IP entre outros, A principio escolheremos a VPC padrão, para o fim de agilidade, mas no próximo desafio, esplicarei como criar uma VPC. Nossa instancia terá as seguintes configurações: 1 Instancia, com Network VPC(default), subnet(default).
4 passo, iremos escolher o tamanho do storage, o free tier libera até 30GB de espaço, então usaremos o seu limite de 30GB.
Caso queira add TAG, está na opção numero 5, colocaremos a key como server e o valor application.
No 6° passo, A configuração do security group, no qual é responsável pela liberação de acesso a instância. Liberaremos as portas 22 e 80.
O 7° passo, nos mostra todo o resumo da instancia que acabamos de criar, após verificarmos se tudo está ok, pode clicar em Lauch.
Toda instância deverá ter um par de chaves, para que possamos acessar, caso perca essa chave, terá que gerar uma nova, pois a AWS não guarda.
Depois que nossa instância estiver rodando, vamos acessar através do ssh utilizando a chave privada e instalaremos o docker, para fazer a instalação do docker, pode serguir o passo a passo no site do proprio docker onde tem a documentação explicando,mas vamos instalar da forma mais fácil utilizando o CURL, a linha de comando é a: curl -fsSL https://get.docker.com | bash, assim que você colocar isso no terminal, rodará um script onde fará a instalação automática.
Após a instalação, vamos atualizar o nosso linux para carregar as configurações mais recentes.
