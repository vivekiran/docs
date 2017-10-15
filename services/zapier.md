---
name: Zapier
slug: zapier
---

After installing add the following configuration to your `config/shield.php` file:

````php
'services' => [
    'zapier' => [
        'driver' => \Shield\Zapier\Zapier::class,
        'options' => [
            'username' => 'your-username',
            'password' => 'your-password',
        ]
    ]
]
````

You can now add the middleware to your routes like so:

````php
Route::middleware('shield:zapier')->post('/hooks/zapier', 'HooksController@zapier');
````
