# Implementação de Regras de Negócio com Drools

<img src="https://i.pinimg.com/originals/0d/14/7c/0d147c411a8ce284e733b4db4294712a.jpg" width="750px" height="400px">

**Este repositório refere-se a um projeto em Java, desenvolvido para a disciplina de Sistemas de Apoio à Decisão do curso de Sistemas de Informação. O projeto tem como objetivo implementar regras de negócio utilizando a biblioteca Drools.**

## Estrutura do Projeto

Inicialmente, foi criado o arquivo `pom.xml` onde foram adicionadas as dependências necessárias para o Drools e SLF4J, conforme orientação em vídeo. A estrutura do projeto inclui as pastas e arquivos Java responsáveis por representar o modelo de CNH, com propriedades como número, nome, quantidade de pontos, data de expiração, entre outros detalhes relevantes.

A classe CNH foi desenvolvida com atributos específicos para armazenar essas informações e servir de base para a aplicação das regras de negócio.

## Implementação das Regras de Negócio

Foi criado um arquivo `.drl` (Drools Rule Language) contendo as regras de negócio que verificam as seguintes condições para cada CNH:

- Se a CNH está expirada.
- Se a CNH acumulou mais de 20 pontos.
- Se a CNH ainda não foi processada.

Cada regra foi definida seguindo as boas práticas recomendadas no vídeo, e o arquivo `.drl` foi configurado para aplicar as condições de validação necessárias para processar o status das CNHs.

## Processamento das CNHs

O código Java responsável pelo envio dos objetos CNH para o Drools foi implementado. Esse código utiliza as regras definidas no arquivo `.drl` para processar e modificar o status das CNHs, marcando-as como válidas ou inválidas, dependendo das condições verificadas. A integração com o Drools permite que o processamento seja automático e eficiente.

## Testes e Validação

A aplicação foi testada com diferentes exemplos de CNHs, conforme demonstrado no vídeo. Utilizamos o `System.out.println` para exibir o resultado final de cada CNH, mostrando o status e a causa da invalidação, como CNH expirada ou excesso de pontos. Todos os testes foram validados para garantir que as regras de negócio estão funcionando conforme esperado.
