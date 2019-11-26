
# aws-IAM-access-key
En este tutorial mostraré los pasos para crear la clave de acceso IAM.
El objetivo es conocer los pasos para obtener la clave de acceso y con ella configurar el acceso a CLI ***Commanda Line Interface***  desde tu terminal o desde CLoud9

## Qué es la clave de acceso IAM access key  ***\(Identity and Access Management)***
- Las claves de acceso son credenciales para un usuario de IAM
- Se componen de dos partes: un ID de clave de acceso ***\(Access Key ID)*** y una clave de acceso secreta ***\(Secret access key)***
- Las claves de acceso sirven para firmar solicitudes y poder utilizar AWS CLI o tener acceso desde programación a la API de AWS (directamente o mediante el SDK de AWS)

## Prerequisitos
1. Contar con un usuario en AWS con permisos para acceder a la programación 

# Pasos para crear la clave de acceso IAM access key

### 1 Con tu usuario IAM entrar a la consola de AWS

 - [X] Selecciona el servicio Amazon **IAM** Identity and Access Management
 - [X] En el menú de lado izquierdo selecciona la opción **Users**
 - [X] Selecciona el **usuario** con permisos para programación 
 - [X] Selecciona la pestaña **\<Security credentials>**
 - [X] Selecciona el botón **\<create access key>**
 - [X] Baja a tu computadora el archivo **.csv**  que contiene las llaves 
 - [X] Copiar en tu block de notas las claves de acceso :notebook:  

### 2 Instalar CLI en tu computadora

````
pip3 install awscli --upgrade --user
aws --version
aws-cli/1.16.51 Python/2.7.10 Darwin/18.2.0 botocore/1.12.41
````

### 3 Desde una terminal o desde Cloud9

 - [X] Necesitas tener lista la clave de acceso 
 - [X] Necesitas saber que región utilizarás, en este ejemplo se utilizará la región de Virginia us-east-1
 
```
aws configure
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: us-east-1
Default output format [None]: text
```
:white_check_mark: si la clave de acceso es correcta, podrás comenzar a utilizar AWS CLI ***Command Line Interface***  

Algunos comandos que puedes utilizar 

```
aws --version
aws ec2 describe-regions
aws ec2 describe-instances
aws configure get region --profile default
asw configure --profile default
aws ec2 describe-instances --profile defaultst-1
Default output format [None]: text

```

# Conclusión

Es muy común utilizar el servicio CLI y las API con el uso de la clave de acceso, pero siempre debemos considerar los problemas de seguridad que tendremos al no tener cuidad en su uso.  Por lo general se recomienda el uso de los roles para lograr accesos seguros determinados para un identidad. 


:raised_hands: @professormartha
