# template php library

Crear diretorio 
nomedoprejeto/
--src/
--composer.json
--run.php

### Cria dentro de src/ a clase Html.php 
```php
namespace Pat; // raiz do documento cada namespace será uma nova pasta
Html
{
    public function hola()
    {
        echo "Hola mundo en español";
    }
}
    
```

### Cria arquivo composer.json 
```json
    {
        "autoload": {
            "psr-4": {"Pat\\": "src/"}
    },
        "require": {}	
    }
```
### Cria a pasta vendor/ com linha de comando para fazer o autoloader das clases
```bach
 composer dump-autoload ou dumpautoload
```

### Cria arquivo run.php

```
namespace Pat\Html;

$htmlObject = new Html();
$htmlObject->saluda();     

 ```

### Executa run.php

```bach 
php run.php    
```
### Baixar arquivo phpcs.phar 
```bach
$ curl -OL https://squizlabs.github.io/PHP_CodeSniffer/phpcs.phar
```
### instala Modulo PEAR
```	
$ sudo pear install PHP_CodeSniffer
```
### Instala code sniffer de forma global
```
$ composer global require "squizlabs/php_codesniffer=*"
```
### Consulta todas as regras PSR2 tipo espacio entre namespace erros de padronização de código
```php phpcs.phar --standard=PSR2 MyClass.php```
### Sumario do php sniffer
```
php phpcs.phar --report=summary --standard=PSR2 src/MyClass.php
```
### Como Especificar o code standard?
PEAR (default)
PHPCS
PSR1
PSR2
Squiz
Zend
