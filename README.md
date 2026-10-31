<div align="center">

# react-hooks-lib

**Six hooks with no dependencies, each with the test that proves it does not leak.**

[![react](https://img.shields.io/badge/react-18%2B-61dafb?style=flat-square&logo=react&logoColor=black)](#quick-start)
[![license](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

</div>

## About

The interesting part of a hook is its cleanup. Each one here has a test
that mounts, unmounts, and asserts that no listener, timer, or observer is
left behind — the failure mode that shows up as a slow memory leak months later
rather than as a failing test on the day.

## Quick start

```bash
git clone https://github.com/irisdomain23/react-hooks-lib
npm install
npm test
```

## Configuration

| Key | Description |
| --- | --- |
| `useDebounced(value, ms)` | debounced mirror of a value |
| `useLocalStorage(key, init)` | persisted state that survives a reload |
| `useMediaQuery(q)` | reactive media-query match |
| `useIntersection(ref, opts)` | visibility observer with cleanup |
| `useInterval(fn, ms)` | `setInterval` that follows the latest callback |
| `useEventListener(t, e, fn)` | listener attached/detached with the element |
## Roadmap

- [ ] React 19 `use()` compatibility check
- [ ] Server-component-safe variants
- [ ] Bundle-size budget in CI

## Contributing

Issues and pull requests are welcome. Please keep changes small and focused,
and add a test for any behaviour change — every repository here ships with a
runnable test suite and no third-party dependencies, so CI is just
`python3 -m unittest` / `bash test_*.sh`.

## License

[MIT](LICENSE)
