# **Documentação de utilização do Framework de automação de testes **

Bibliotecas utilizadas:

[!
(https://junit.org/junit4/) [![gherkin](https://img.shields.io/badge/gherkin-2.12.2-brightgreen.svg)](https://cucumber.io/docs/gherkin/) [![restassured](https://img.shields.io/badge/restassured-2.9.0-brightgreen.svg)](https://github.com/rest-assured/rest-assured/wiki/ReleaseNotes29) 
[!
[selenium](https://img.shields.io/badge/selenium-3.141.59-blue.svg)](https://www.seleniumhq.org/)


# Como escrever seus testes utilizando o framework:


1. Primeiro é necessário ter o [git](https://git-scm.com/) e o [NodeJs](https://nodejs.org/en/download/) instalado e ter realizado o clone do repositório da branch [master]

  Para clonar o repositório:
* git clone + url 

2.  Após clonar o repositório, entre na pasta que você acabou de clonar, verifique se você está na mesma pasta onde contém o arquivo "pom.xml" e execute o seguinte comando:

  * mvn install -Dmaven.test.skip=true  (Este comando será o responsável por instalar as dependências do framework).

3. Após os passos 1 e 2, faço o manuseio do projeto via eclipseOxygen + Java (jdk-8u202-windows-x64)

Ao acessa o projeto, basta acessar: src/test/java > com.executar > CucumberExecuteTest.java e clicar em Run CumcumberExecuteTest



Foi criada uma Feature com 9 cenários de testes e 28 stpes de validação:



Feature: Validar funcionalidades do site automationexercise
  	Eu como usuario desejo acessar o site automationexercise
	E visualizar um formulario de login
	E realizar o preenchimento do login para dar andamento
	E realizar a buscar de um produto
  	E incluir produto no carrinho
	E validar os produtos incluídos no carrinho na tela de pagamento.
	

	@automationexercise
	Scenario: Validar o carregamento do site na tela
		Given que acesso o site automationexercise 
		When aguardo o site automationexercise carregar
		Then valido a url acessada

	@automationexercise
	Scenario: Validar o preenchimento do campo email na tela
		Given que visualizo o campo email 
		When clico no campo email
		Then escrevo o e-mail
		
	@automationexercise
	Scenario: Validar o preenchimento do campo senha na tela
		Given que visualizo o campo senha 
		When clico no campo senha
		Then escrevo a senha
		
	@automationexercise
	Scenario: Validar a funcionalidade do botao login
		Given que visualizo o botao login na tela
		When clico no botao login 
		Then deve realizar o login no portal
		
	@automationexercise
	Scenario: Validar o menu produtos
		Given que visualizo o menu produtos na tela
		When clico em produtos 
		Then deve carregar a pagina de produtos
		
	@automationexercise
	Scenario: Validar a busca de produtos
		Given que visualizo a barra de busca
		When clico na opcao pesquisar produto
		Then escrevo o nome do produto
		And clico no botao lupa
		
	@automationexercise
	Scenario: Validar o retorno da busca de produtos
		Given que visualizo o titulo de retorno
		When rolo o mouse para baixo
		Then confirmo o retorno do produto na tela
		
	@automationexercise
	Scenario: Validar adicao do produto no carrinho
		Given que clico em adicionar no carrinho
		When exibir o modal de adicionado em tela
		Then clico em view cart
		
	@automationexercise
	Scenario: Validar itens no carrinho
		Given que estou na pagina vier cart
		When exibir os itens na tela
		Then confiro o nome do produto
		

#### Qualquer dúvida sobre a utilização do framework, entre em contato:

Thais de Lima Santos - thais_tlsan@hotmail.com



