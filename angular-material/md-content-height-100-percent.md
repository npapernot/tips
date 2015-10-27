# Height of `md-content` not taking 100% of parent

To solve issues where a md-content is not taking 100% of its parent height, try the following:

1. Define the parent with the attribute `layout-fill`
2. Make sure to include first an md-content with `flex` and `layout="column"`
3. Then and only then include a row md-content
