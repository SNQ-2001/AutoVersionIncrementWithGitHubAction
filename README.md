# メモ

### 一発でリリースPRを作成する
以下のURLを押す

https://github.com/SNQ-2001/AutoVersionIncrementWithGitHubAction/compare/main...develop?quick_pull=1&title=%5B%E5%BF%85%E9%A0%88%5D%E3%82%BF%E3%82%A4%E3%83%88%E3%83%AB%E3%81%AB%E3%83%AA%E3%83%AA%E3%83%BC%E3%82%B9%E3%81%99%E3%82%8B%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B3%E3%82%92%E5%85%A5%E5%8A%9B%E3%81%97%E3%81%A6%E3%81%8F%E3%81%A0%E3%81%95%E3%81%84&labels=%E3%83%AA%E3%83%AA%E3%83%BC%E3%82%B9

# 参考記事

### アプリのバージョン取得
https://qiita.com/hirothings/items/8b417b2efe2e1c1bc0ac

### github-actions[bot]にコミットさせる
https://scrapbox.io/nwtgck/GitHub_Actions%E3%81%AE%E3%83%9C%E3%83%83%E3%83%88%E3%81%8C%E3%82%B3%E3%83%9F%E3%83%83%E3%83%88%E3%81%97%E3%81%9F%E3%82%88%E3%81%86%E3%81%AB%E3%82%A2%E3%82%A4%E3%82%B3%E3%83%B3%E3%82%92%E3%81%A4%E3%81%91%E3%82%8B%E3%81%AB%E3%81%AF%E3%83%A1%E3%83%BC%E3%83%AB%E3%81%AB%E3%80%8Cgithub-actions%5Bbot%5D@users.noreply.github.com%E3%80%8D%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%99%E3%82%8C%E3%81%B0%E8%89%AF%E3%81%84

### github-actions[bot]がコミットできない
Read and writeに変更

<img width="844" alt="スクリーンショット 2023-10-24 16 36 39" src="https://github.com/SNQ-2001/AutoVersionIncrementWithGitHubAction/assets/84154073/731cef65-16cf-4124-bc24-4ac35be9e672">

https://zenn.dev/osawa_koki/articles/a63b96a2707a8f

Organizationアカウントだと上の設定ができない
https://github.com/orgs/community/discussions/57244

個別に設定する方がいいらしい
https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#permissions
https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idpermissions


こんな感じ
```yml
permissions:
  actions: write
  checks: write
  contents: write
```

### クエリ パラメーターを使って pull request を作成する
https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/using-query-parameters-to-create-a-pull-request
