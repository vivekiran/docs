---
name: Recurly
slug: recurly
---

After installing add the following configuration to your `config/shield.php` file:

````php
'services' => [
    'reculry' => [
        'driver' => \Shield\Recurly\Recurly::class,
        'options' => [
            'username' => 'your-custom-http-auth-username',
            'password' => 'your-custom-http-auth-password,
        ]
    ]
]
````

You can now add the middleware to your routes like so:

````php
Route::middleware('shield:recurly')->post('/hooks/recurly', 'HooksController@recurly');
````