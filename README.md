# Welcome to [Slidev](https://github.com/slidevjs/slidev)!

To start the slide show:

- `pnpm install`
- `pnpm dev`
- visit <http://localhost:3030>

Edit the [slides.md](./slides.md) to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).

Для заголовка с изображением `images/header.png` используйте компонент:

```vue
<SlideHeader title="Проблема" />
```

Шапка прижата к верхнему краю слайда и занимает всю ширину. Название
располагается на светлой области справа от логотипа. Для длинных названий
можно уменьшить шрифт: `<SlideHeader title="Розмір ринку та можливості" font-size="24px" />`.
Компонент заменяет обычный заголовок слайда. При добавлении содержимого
оставляйте сверху место для шапки (около 145 px при стандартной ширине слайда).
