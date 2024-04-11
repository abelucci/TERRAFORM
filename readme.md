# **TERRAFORM**

Primeramente, instalar paquete desde el repositorio oficial de terraform.

* Verificar instalación:

  ```
  vagrant --version
  ```

  Crear la estructura mediante IaC, main.tf, provider.tf, variables.tf
* Inicializar terraform:

  ```
  terraform init -upgrade
  ```
* Verificar el plan:

  ```
  terraform plan -out main.tfplan
  ```
* Aplicar el plan:

  ```
  terraform apply main.tfplan
  ```
* Verificar antes de borrar los recursos:

  ```
  terraform plan -destroy -out main.destroy.tfplan
  ```
* Aplicar:

  ```
  terraform apply main.destroy.tfplan
  ```
* Conexión ssh modo seguro con llave publica y privada:

  ```
  ssh -i linuxkey.pem azureuser@<IP PUBLIC>
  ```

  Aclaración: verificar los permisos de acceso hacia la llave linuxkey creada mediante terraform.

  También excluir archivos que sean pesados o que no haga falta subir al repo en github, usar .gitignore

# **CREACIÓN DE VM LINUX**

[Docs creación VM](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-terraform?tabs=azure-cli)
