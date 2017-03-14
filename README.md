# template php library

Crear diretorio 
nomedoprejeto/
--src/
--composer.json
--run.php


### criar composer.json 
```json
    {
        "autoload": {
            "psr-4": {"Pat\\": "src/"}
    },
        "require": {}	
    }
```
### cria a pasta vendor com linha de comando
```bach
 composer dump-autoload ou dumpautoload
```
### criar dentro de src/Html.php
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
### criar arquivo run.php

```
namespace Pat\Html;

$htmlObject = new Html();
$htmlObject->saluda();     

 ```