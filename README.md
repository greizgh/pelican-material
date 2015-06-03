# pelican-material

Material is a [pelican](http://blog.getpelican.com/) theme based on [Materialize](http://materializecss.com/), a material design framework.

## Configuration

This template uses a cutom filter to sort tags by article count. You need to add this to your config:

```python
JINJA_FILTERS = {
    'sort_by_article_count': partial(
        sorted,
        key=lambda tags: len(tags[1]),
        reverse=True)} # reversed for descending order
```

## License

MIT
