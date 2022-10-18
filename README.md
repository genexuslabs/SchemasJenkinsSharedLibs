# Auto-completion for Properties.yaml files on Visual Studio Code

To make building properties files easier we are going to use a new tool called json.schemas.

This tool allow us to have a kind of syntax validation or auto-completion as you work on your properties files and thus be able to have a better experience in the development.

In this case we are going to be using the schemas to autocomplete and correct the syntax of the property files that provide us with the necessary data to be able to build Apps with the Jenkins Shared Libraries developed by GeneXus 

For more information about the libraries you can check here [Shared Libraries](https://iwiki.genexus.com/wiki.aspx?31147,KBBuilder+Jenkins+Shared+Libraries)



## How it Works ?

### VS Code and JSON Schema
VS Code has the ability to display auto-complete suggestions for JSON and YAML files out of the box. It uses JSON schemas 

#### JSON Schema 
Is a vocabulary that allows you to annotate and validate JSON and YAML documents. https://json-schema.org

There is a public available [PDF](https://json-schema.org/understanding-json-schema/UnderstandingJSONSchema.pdf) that covers all the options.

## Setting up development environment for Visual Studio Code
To get VS Code auto-complete your Properties files, first, you need a YAML extension for VS Code. In this case we will need [Redhat YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) extension.

### Install YAML Plugins
First thing you need to download YAML Language plugin.

Open `Extensions` by going to `File->Preferences->Extensions` or use keyboard shortcut `SHIFT+CMD+X`

Look for YAML and install YAML Language Support by Red Hat

### Apply JSON Schemas on your YAML files
Depending on the type of file we are working with, we will have a schema that will help us.

- Properties.yaml

- Environmentname.yaml

- DeploymentUnits.yaml

    - DockerImage.yaml

    - Aws-Serverless-Du.yaml

    - Angular-Service>.yaml

    - Services.yaml

    - Dockerdaemon.yaml


To implement it in our file we will have to place the following signature on the first line of our file: `# yaml-language-server: $schema=https://raw.githubusercontent.com/genexuslabs/SchemasJenkinsSharedLibs/main/Schemas/schemasrefs.json`

<img src="images\sgnatureyaml.png">


Pressing `ctrl + space` will show us the options to autocomplete




