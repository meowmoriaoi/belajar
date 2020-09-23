# View Layout

> app/Controllers/Layout.php

```php

<?php

namespace App\Controllers;

class Layout extends BaseController
{
    public function index()
    {
        return view('belajar');
    }
}

```

> app/Views/belajar.php

```php

<?php

<?= $this->extend('Layouts/main') ?>

<?= $this->section('content') ?>
<ul>
    <li>Farras</li>
    <li>Agda</li>
    <li>Munggaran</li>
</ul>
<?= $this->include('Layouts/tambahan') ?>
<?= $this->endSection() ?>

```

> app/Views/Layouts/main.php

```php

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <h1>Identitas</h1>
    <?= $this->renderSection('content') ?>
    <h2>Big Match!!</h2>
</body>

</html>

```