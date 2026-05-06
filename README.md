# flask-ujson

A [Flask][]/[Quart][] JSON provider using the fast [ujson][] library. Using
this provider will significantly speed up reading JSON data in requests and
generating JSON responses.

[flask]: https://flask.palletsprojects.com
[quart]: https://quart.palletsprojects.com
[ujson]: https://github.com/ultrajson/ultrajson

## Example

```python
from flask import Flask
from flask_ujson import UjsonProvider

app = Flask(__name__)
app.json = UjsonProvider(app)
```

## Official statement from the UltraJSON library:

> [!WARNING]
> UltraJSON's architecture is fundamentally ill-suited to making changes without
> risk of introducing new security vulnerabilities. As a result, this library
> has been put into a *maintenance-only* mode. Support for new Python versions
> will be added and critical bugs and security issues will still be
> fixed but all other changes will be rejected. Users are encouraged to migrate
> to [orjson](https://pypi.org/project/orjson/) which is both much faster and
> less likely to introduce a surprise buffer overflow vulnerability in the
> future.

Statement can be seen here: [https://github.com/ultrajson/ultrajson](https://github.com/ultrajson/ultrajson)

With this in mind we encourage you to either migrate, or use: [https://github.com/pallets-eco/flask-orjson](https://github.com/pallets-eco/flask-orjson) instead.
