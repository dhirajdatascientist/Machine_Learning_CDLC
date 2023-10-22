## What is Markers?

In Python's `matplotlib` library, the `scatter` and `plot` functions provide various markers to represent data points. Here are some common marker options:

1. `'.'`: Point marker
2. `','`: Pixel marker
3. `'o'`: Circle marker
4. `'v'`: Triangle down marker
5. `'^'`: Triangle up marker
6. `'<'`: Triangle left marker
7. `'>'`: Triangle right marker
8. `'1'`: Tripod down marker
9. `'2'`: Tripod up marker
10. `'3'`: Tripod left marker
11. `'4'`: Tripod right marker
12. `'s'`: Square marker
13. `'p'`: Pentagon marker
14. `'*'`: Star marker
15. `'h'`: Hexagon marker
16. `'H'`: Rotated hexagon marker
17. `'+'`: Plus marker
18. `'x'`: X marker
19. `'D'`: Diamond marker
20. `'d'`: Thin diamond marker
21. `'|'`: Vertical line marker
22. `'_'`: Horizontal line marker

There are other specialized markers available, and you can also create custom markers, but the above list covers the most common ones.

To use these markers, you simply pass the desired marker string to the `marker` argument in `plt.scatter` or `plt.plot`. For instance, to plot with square markers, you'd do something like:

```python
import matplotlib.pyplot as plt
plt.plot([1, 2, 3], [1, 2, 3], marker='s')
plt.show()
```

This would plot three points with square markers.