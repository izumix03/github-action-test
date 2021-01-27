# github-action-test

```shell
mkdir -p .github/workflows/  
touch .github/workflows/learn-github-actions.yml
```

`.github/workflows/learn-github-actions.yml` を編集
```yaml
name: learn-github-actions
on: [push]
jobs:
  check-bats-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v1
      - run: npm install -g bats
      - run: bats -v
```
