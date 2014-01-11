# EddieJaoude\Zf2Logger

#### Zend Framework 2 Event Logger.
#### Log incoming Requests &amp; Response data.

---

## Installation via Composer

### Steps 

#### 1. Add to composer.
```
    "require" : {
        "eddiejaoude/zf2Logger" : "dev-master"
    }
```

#### 2. Create `zf2Logger.global.php` in `config/autoload` with configuration (/config/module.config.php.dist)
```
    /module.config.php.dist to /config/autoload/zf2Logger.global.php
```

#### 3. Add module to application config (/config/application.config.php)
```
   ...
   'modules' => array(
        'EddieJaoude\Zf2Logger',
   ),
   ...
```

Then you are good to go. All requests & responses will be logged.

---

## Example output

### Request

```
2014-01-09T16:28:23+00:00 DEBUG (7): Array
(
    [zf2.local] => Array
        (
            [Request] => Zend\Uri\Http Object
                (
                    [validHostTypes:protected] => 19
                    [user:protected] =>
                    [password:protected] =>
                    [scheme:protected] => http
                    [userInfo:protected] =>
                    [host:protected] => zf2.local
                    [port:protected] =>
                    [path:protected] => /api/user
                    [query:protected] =>
                    [fragment:protected] =>
                )

        )

)
```

### Response

```
2014-01-09T16:28:24+00:00 DEBUG (7): Array
(
    [zf2.local] => Array
        (
            [Response] => Array
                (
                    [statusCode] => 200
                    [content] => {"total":2,"data":[{"id":"12345 ...
                    ...
                )
        )
)
```

---

## What Next...

* Additional outputs, same as Zend\Logger
* Additional events
* Filtering

---

## Resources

* Github
* Packagist
* Zend Framework 2 Modules
* Travis CI

