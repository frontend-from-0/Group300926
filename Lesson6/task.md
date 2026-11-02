# Lesson 6 – Dashboard page layout with CSS Grid

Today we build the layout of an analytics dashboard ("Overview" page) using CSS Grid.

## Page layout (outer grid)

```text
+--------------+-----------------------------+---------------+
|              |  controls bar               |               |
|   left       +-----------------------------+    right      |
|   sidebar    |  page header ("Overview")   |    sidebar    |
|  (navigation)+-----------------------------+               |
|              |  main content (inner grid)  |               |
|              |                             |               |
+--------------+-----------------------------+---------------+
```

- Left sidebar: between 200px and 250px wide, full page height.
- Right sidebar: between 250px and 300px wide, full page height.
- Middle column takes the remaining space.

## Main content (inner grid, 4 columns)

```text
+-----------+-----------+-----------+-----------+
|  Views    |  Visits   | New Users | Active    |
|           |           |           | Users     |
+-----------+-----------+-----------+-----------+
|  Total Users (3 columns)          | Traffic   |
|                                   | by Website|
+-----------------------+-----------+-----------+
|  Traffic by Device    |  Traffic by Location  |
+-----------------------+-----------------------+
|  Marketing & SEO (full width)                 |
+-----------------------------------------------+
```

We will practise: `display: grid`, `grid-template-columns` / `grid-template-rows`, `minmax()`, `fr`, named grid lines, `grid-template-areas` / `grid-area`, `grid-column` with `span` and `-1`, and nested grids.
