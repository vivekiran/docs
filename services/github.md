---
name: GitHub
slug: github
---

After installing add the following configuration to your `config/shield.php` file:

````php
'services' => [
    'github' => [
        'driver' => \Shield\GitHub\GitHub::class,
        'options' => [
            'token' => 'your-webhook-token'
        ]
    ]
]
````

You can now add the middleware to your routes like so:

````php
Route::middleware('shield:github')->post('/hooks/github', 'HooksController@github');
````
