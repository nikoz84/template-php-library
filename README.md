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

curl -OL https://squizlabs.github.io/PHP_CodeSniffer/phpcs.phar
	
pear install PHP_CodeSniffer

composer global require "squizlabs/php_codesniffer=*"

php phpcs.phar --standard=PSR2 MyClass.php

php phpcs.phar --report=summary --standard=PSR2 MyClass.php

Especificar o code standard
PEAR (default)
PHPCS
PSR1
PSR2
Squiz
Zend
