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