# Use meaningful class names

When writing a lot of CSS, it's easy to get lazy and start to write class names that aren't so great for future you or for your team. `big-red-header` might make sense today, but when the design changes in a few months, and the header becomes orange, `big-red-header` with `color: orange;` may not seem like such a good idea.

When you can, it's better to describe the purpose rather than the properties. `main-header` or `header-category` can be a better description of what the class does, and can be more reusable. The class name doesn't tell you **what the content looks like**, it tells you **what it does**.
