# Takes

Сайт магазина ИИ-рецептов для видео и контента. Загружаешь подкаст или лекцию, выбираешь рецепт и получаешь нарезки, титры и тексты. Каждый рецепт проходит автоматическую проверку качества, не прошёл — деньги возвращаем.

Сейчас это витрина с демо-данными: цифры проверок в интерфейсе — демо до запуска и подписаны как демо.

## Маршруты

| Путь | Что там |
|---|---|
| `/` | Лендинг |
| `/recipes` | Каталог рецептов с поиском и фильтрами |
| `/recipes/[slug]` | Страница рецепта |
| `/design` | Живой стайлгайд «Дизайн-система Takes» |

## Стек

- Next.js 16 (App Router, Turbopack, Cache Components), React 19, TypeScript strict
- Tailwind CSS v4, токены в `src/styles/tokens.css`
- `motion/react` для анимаций, Lenis для плавного скролла мышью
- `lucide-react` для иконок
- Шрифты через `next/font/google`: Unbounded, Inter, JetBrains Mono
- pnpm

## Запуск

```bash
pnpm install
pnpm dev      # http://localhost:3000
pnpm build    # продакшен-сборка
pnpm start    # запуск собранного
pnpm lint     # eslint
```

Проверка типов: `pnpm exec tsc --noEmit`.

## Структура

```
src/
  app/                 маршруты, layout, not-found, icon.svg
  components/
    ui/                атомы: Button, Badge, Container, Section, Logo, Viewfinder, RecDot, Timecode
    motion/            Reveal, SplitText, Magnetic, TiltCard, Marquee, CountUp, Scramble, BeforeAfter
    layout/            Header, Footer, ThemeToggle
    sections/          секции страниц
    clips/             анимированные клипы без футажа
  content/             тексты и данные, никакого копирайта в JSX
  lib/                 cn, токены движения, хуки, форматирование
  styles/tokens.css    дизайн-токены
```

## Документация

- [CONVENTIONS.md](./CONVENTIONS.md) — правила кода, SSR, анимаций, копирайта и замороженные контракты.
- [DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md) — дизайн-система и QA-чеклист из 15 пунктов.
- Вживую — на странице `/design`.
# takes
