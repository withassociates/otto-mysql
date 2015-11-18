[MySQL][1] application for [Otto][2].

## Usage

Add as a dependency in your Appfile:

```
application {
    name = "example-app"

    dependency {
        source = "github.com/withassociates/otto-mysql"
    }
}
```

Configure Rails app to use the containerized DB:

```rb
# config/database.yml

development:
  adapter: mysql2
  encoding: utf8
  pool: 5
  username: root
  password:
  host: mysql.service.consul
```

**NOTE:**

Does not include client tools such as mysql and mysqldump.

[1]: https://www.mysql.com/
[2]: https://ottoproject.io/
