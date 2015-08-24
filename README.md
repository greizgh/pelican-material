# pelican-material

Material is a [pelican](http://blog.getpelican.com/) theme based on [Materialize](http://materializecss.com/), a material design framework.

## Dependencies

Dependencies are managed through [bower](http://bower.io/).
Once you have bower, you are only one command away to use the theme.

Run this command from the `static` directory:

    bower install

## Configuration

This template uses a cutom filter to sort tags by article count. You need to add this to your config:

```python
from functools import partial
JINJA_FILTERS = {
    'sort_by_article_count': partial(
        sorted,
        key=lambda tags: len(tags[1]),
        reverse=True)} # reversed for descending order
```

You will probably want to use [pelican-materialbox](https://github.com/greizgh/pelican-materialbox), a pelican plugin to use [materialboxed](http://materializecss.com/media.html#materialbox) from Materialize.

## License

MIT
