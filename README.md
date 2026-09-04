# react-hooks-lib

Three React hooks I use across every project — typed, dependency-free, and
small enough to read in one sitting.

## Hooks

- **`useDebounce(value, delay)`** — returns a value that updates only after
  `delay` ms of no changes. Use it on search inputs before you hit an API.
- **`useLocalStorage(key, initial)`** — read/write a value in localStorage
  with the same API as `useState`. Falls back to the initial value when
  storage is unavailable (private mode, SSR).
- **`useMediaQuery(query)`** — subscribes to a CSS media query and re-renders
  when it changes. Use it for responsive logic that cannot live in CSS alone.

## Usage

```ts
import { useDebounce, useLocalStorage, useMediaQuery } from "react-hooks-lib";

const debounced = useDebounce(searchTerm, 300);
const [theme, setTheme] = useLocalStorage("theme", "light");
const isWide = useMediaQuery("(min-width: 768px)");
```

## Why

These are not clever. They are the hooks I got tired of re-deriving, kept in
one place with types and JSDoc so I can import them without thinking. No
runtime dependencies beyond React.

## License

MIT
