#### MIXINS!

### When to Use @extend

(EXAMPLE: a replacement for global classes or "Style Mixins")

- **Share styles across selectors with concise CSS output.**
- **Build a style structure with inheritance in mind.**
- **Selectors don’t need to vary in their properties.**

### When to Use @include

(EXAMPLE: a replacement for shorthands/utility classes or "Utility Mixins")

- **Need dynamic styles with arguments.**
- **Create utility mixins or reusable styles with customizability.**
- **Want more control over where and how styles are applied without selector merging.**

### Improvements

1. **For shared base styles, use @extend to minimize duplication.**
2. **For customizable elements (e.g., buttons with varying colors), prefer @include with parameters for flexibility.**
3. **Evaluate CSS output size: while @extend minimizes size, @include provides modular flexibility. Choose based on the project's goals for performance and maintainability.**
