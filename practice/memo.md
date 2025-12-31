- package.jsonを生成するコマンド
```
npm init --yes
```
- "type": "module",はそのパッケージ配下の .js ファイルを「ES Modules（ESM）」として扱うための設定

- tsconfig.jsonの準備を行う必要がある
- tsconfigはTSコンパイラに対する設定を記述したファイル
- 下記コマンドでtsconfig.jsonを生成
```
npx tsc --init
```
