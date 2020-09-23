# View Cells

> app/Libraries/Web.php

```php

<?php

namespace App\Libraries;

class Web
{
    public function postItem()
    {
        $items = [
            'language' => 'English',
            'items' => ['Sange and Yasha', 'Mask of Madness', 'Daedalus', 'Monkey King Bar']
        ];


        return view('Components/post_item', $items);
    }
}

```

>  app/Views/Components/post_item.php

```php

<ul>
    <?php foreach ($items as $item) : ?>
        <li><?= $item ?></li>
    <?php endforeach; ?>
</ul>

<h3><?= $language ?></h3>

```

>  app/Views/Pages/footer.php

```php

<?= view_cell('\App\Libraries\Web::postItem') ?>

</body>

</html>

```