# squawk-255-demo

Temporary repo for https://github.com/sbdchd/squawk/issues/255

## Steps to reproduce

1. Clone this repo
2. Setup pre-commit hooks

```sh
npm i
npm run prepare
```

3. Add a file `migrations/example.sql` with `SELECT 1;`
4. `npm run lint` and notice that all linting passes
5. `git add -A && git commit -m 'Test'`

## Expected

- husky runs lint-staged and successfully lints the migration using squawk

## Actual

- squawk hangs:
  <img width="495" alt="Screen Shot 2023-01-26 at 9 25 36 AM" src="https://user-images.githubusercontent.com/2145098/214862897-baede752-ad4d-48a6-88ec-8fc954260d68.png">
