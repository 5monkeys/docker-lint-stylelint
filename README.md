# stylelint (Alpine)


Minimal stylelint image using Alpine.


# Usage

## Example usage via Docker Compose

### docker-compose.yml

```yaml
version: "2"
services:
  lint-css:
    image: 5monkeys/lint-stylelint
    volumes:
      - "./.stylelintrc.js:/.stylelintrc.js"
      - ".:/code"
    command: /code/src/radar/static/{fonts,scss}/**/*.scss --syntax scss
```

### Running

```bash
$  docker-compose run --rm lint-css
```
