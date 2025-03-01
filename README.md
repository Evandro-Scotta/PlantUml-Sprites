1. Incluindo a biblioteca C4
Primeiro, você deve incluir a biblioteca C4 do PlantUML para criar diagramas seguindo o modelo de C4. No início do seu código PlantUML, adicione o seguinte:

plantuml
Copiar
Editar
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml
!define ICONS https://raw.githubusercontent.com/Evandro-Scotta/PlantUml-Sprites/refs/heads/develop/Icons
2. Definindo Containers e Ícones
Em seguida, defina os containers e associe os ícones a eles. No exemplo abaixo, mostramos como incluir uma imagem (usando o sprite) no container Aplicação Web:

plantuml
Copiar
Editar
@startuml

!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml
!define ICONS https://raw.githubusercontent.com/Evandro-Scotta/PlantUml-Sprites/refs/heads/develop/Icons

HIDE_STEREOTYPE()

System_Boundary(system, "Sistema E-Commerce") {
    Container(webapp, "Aplicação Web", "React.js", "Plataforma usada pelos clientes.") {
        webapp : <img:ICONS/salesforce.png>
    }
}

@enduml
3. Gerando o Diagrama
Depois de adicionar o código PlantUML, você pode gerar o diagrama usando o PlantUML. A saída será um diagrama de containers, onde o container Aplicação Web será representado com o ícone do Salesforce, como mostrado no exemplo.

4. Personalização
Você pode personalizar o ícone e o estilo do seu diagrama de várias maneiras:

Alterar ícones: Basta trocar o caminho do ícone no parâmetro <img:ICONS/salesforce.png> para outro ícone disponível no repositório.
Definir outros containers: Além do container Aplicação Web, você pode adicionar outros containers como Aplicação Mobile, Banco de Dados, etc., e associar a eles ícones conforme necessário.
Referências
C4-PlantUML - Biblioteca para diagramas no estilo C4 Model.
PlantUml-Sprites - Repositório com ícones para usar nos diagramas.
Contribuições
Sinta-se à vontade para contribuir com melhorias, novos ícones ou exemplos. Para isso, basta abrir um pull request ou um issue.