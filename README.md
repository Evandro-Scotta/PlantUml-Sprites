<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

  <h1>Como usar ícones e imagens com PlantUML para C4 Model</h1>

  <p>Este repositório contém exemplos de como utilizar imagens e sprites com o PlantUML para criar diagramas de arquitetura no estilo <strong>C4 Model</strong>.</p>

  <h2>Pré-requisitos</h2>
  <ul>
    <li><strong>PlantUML</strong>: Ferramenta para gerar diagramas a partir de código. Você pode usá-lo localmente ou via extensões para IDEs, como <a href="https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml" target="_blank">VS Code</a> ou <a href="https://plugins.jetbrains.com/plugin/7017-plantuml-integration" target="_blank">IntelliJ IDEA</a>.</li>
    <li><strong>Acesso aos ícones e sprites</strong>: Estamos utilizando os ícones do repositório <a href="https://github.com/Evandro-Scotta/PlantUml-Sprites" target="_blank">PlantUml-Sprites</a>, que são usados para personalizar o diagrama.</li>
  </ul>

  <h2>Exemplo de Uso</h2>

  <h3>1. Incluindo a biblioteca C4</h3>
  <p>Primeiro, inclua a biblioteca <strong>C4</strong> no código PlantUML, logo no início:</p>

  <pre id="codeSnippet">
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml
  </pre>

<h3>1. Incluindo imagens</h3>
  <p>Após incluir a biblioteca do <strong>C4</strong> vamos incluir o link para poder utilizar as imagens deste repositório. </p>
  <p>Substitua ICONS, logo após o !define, pelo nome que achar mais apropriado</p>
  
  <pre id="codeSnippet">
!define ICONS https://raw.githubusercontent.com/Evandro-Scotta/PlantUml-Sprites/refs/heads/develop/Icons
  </pre>

  <h3>2. Definindo Containers e Ícones</h3>
  <p>Defina os containers do seu sistema e associe ícones a eles. No exemplo abaixo, mostramos como associar um ícone do Salesforce a um container da "Aplicação Web":</p>

  <pre id="codeSnippet">
@startuml

!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml
!define ICONS https://raw.githubusercontent.com/Evandro-Scotta/PlantUml-Sprites/refs/heads/develop/Icons

HIDE_STEREOTYPE()

System_Boundary(system, "Sistema E-Commerce") {
    Container(webapp, "Aplicação Web", "React.js", "Plataforma usada pelos clientes.", $sprite="img:ICONS/salesforce.png")
}

@enduml
  </pre>

  <h3>3. Gerando o Diagrama</h3>
  <p>Depois de adicionar o código PlantUML, você pode gerar o diagrama usando o PlantUML. A saída será um diagrama de containers, onde o container "Aplicação Web" será representado com o ícone do Salesforce.</p>

  <h3>4. Personalização</h3>
  <p>Você pode personalizar o ícone e o estilo do seu diagrama de várias maneiras:</p>
  <ul>
    <li><strong>Alterar ícones:</strong> Para mudar o ícone, basta substituir o caminho do ícone, como <code>ICONS/salesforce.png</code>, pelo ícone desejado disponível no repositório.</li>
    <li><strong>Adicionar mais containers:</strong> Você pode adicionar containers como "Aplicação Mobile", "Banco de Dados", etc., e associar ícones a eles.</li>
  </ul>

  <h2>Referências</h2>
  <ul>
    <li><a href="https://github.com/plantuml-stdlib/C4-PlantUML" target="_blank">C4-PlantUML</a> - Biblioteca para diagramas no estilo C4 Model.</li>
    <li><a href="https://github.com/Evandro-Scotta/PlantUml-Sprites" target="_blank">PlantUml-Sprites</a> - Repositório com ícones para usar nos diagramas.</li>
  </ul>

  <h2>Contribuições</h2>
  <p>Sinta-se à vontade para contribuir com melhorias, novos ícones ou exemplos. Para isso, basta abrir um pull request ou um issue.</p>

</body>
</html>
