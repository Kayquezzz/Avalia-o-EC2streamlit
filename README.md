# Avalia-o-EC2streamlit

Como fiz o projeto? Kayque Ricardo de Souza Alves.

Primeiro, criei uma instância EC2 na AWS usando a imagem Ubuntu 22.04, escolhi o tipo t2.micro pra ficar grátis e criei um par de chaves (.pem) pra poder acessar a máquina pelo SSH.

Configurei o grupo de segurança liberando as portas 22 (pra acessar pelo terminal) e a 8501, que é a porta padrão do Streamlit, pra poder acessar o app pelo navegador.

Usei o Git Bash no meu computador pra acessar a instância via SSH, passando a chave .pem e o IP público da máquina.

Depois que entrei na instância, atualizei os pacotes do Ubuntu, instalei o Python3, pip, e criei um ambiente virtual pra organizar as bibliotecas.

Ativei o ambiente virtual e instalei o Streamlit, pandas e matplotlib, que eu ia usar no app.

Criei o arquivo app.py(pelo mkdir) com o código Python que lê um arquivo CSV e gera um gráfico mostrando a distribuição dos alunos por status no processo seletivo.

Enviei o arquivo CSV do meu computador pra dentro da pasta do projeto na EC2 usando o comando scp pelo Git Bash também.

Rodei o Streamlit na instância, liberando ele pra escutar na porta 8501 em todos os IPs (0.0.0.0).

Por fim, abri o navegador, coloquei o IP público da instância com a porta 8501, e consegui acessar meu app rodando na nuvem, mostrando o gráfico interativo.
