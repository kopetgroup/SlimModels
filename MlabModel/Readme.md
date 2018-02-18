# Mlab Api Model

18 februari 2018
```

/** MLAB Model */
$container['MlabModel'] = function ($container) {

  $api = '{apikey}';
  $db = '{database}';

  $mod  = new App\Model\MlabModel($api,$db);
  return $mod;

};


/*
  Controller
*/
$container['App\Controller\NameController'] = function ($container) {
  $model    = $container->get('MlabModel');
  return new App\Controller\NameController($model);
};

```
