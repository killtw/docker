# Docker files
For development

## Services
* Mariadb
* Redis
* ElasticSearch

## Usage
### services
``` bash
docker-compose up -d redis mariadb elasticsearch
```

### node
``` bash
docker run -it --rm -v $(PWD):/workspace killtw/workspace node
```

### npm
``` bash
docker run -it --rm -v $(PWD):/workspace killtw/workspace npm
```

### bower
``` bash
docker run -it --rm -v $(PWD):/workspace killtw/workspace gulp
```

### gulp
``` bash
docker run -it --rm -v $(PWD):/workspace killtw/workspace gulp
```

## License

This is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
