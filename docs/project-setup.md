
## Project setup

## create submodule
mvn archetype:generate -DgroupId=com.saral -DartifactId={module-name}

## Run project

## Sample request for diagram
graph TD 
    A[Client] --> B[Load Balancer] 
    B --> C[Server01] 
    B --> D[Server02]

## Sample Mermaid template
    C4Context
      title Console Application: App1
      Boundary(App1,"Commands") {
        System(Print, "Print", "Print the provided argument")
        System(Help, "Help", "Print a help message")
        System(Grep, "Grep", "Search a given string in the given file path")
      }

## Java docs
- Run following command to generate java docs
`mvn javadoc:javadoc`
- It will generate java docs at following location
`target/reports/apidocs/`
