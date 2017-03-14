# template php library

Crear diretorio 
nomedoprejeto/
--src/
--composer.json
--run.php


### criar composer.json cria a pasta vendor dump-autoload ou dumpautoload
```json
    {
        "autoload": {
            "psr-4": {"Pat\\": "src/"}
    },
        "require": {}	
    }
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