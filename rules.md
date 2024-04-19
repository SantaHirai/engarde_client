# ルール

プルリクエストをマージ後、これら↓の修正をするのはアレなので、よろしくお願いします。

## コーディングに関するルール

- ファイルの最後に空行を必ず付けてください。
- VSCodeであれば`Alt + Shift + F`で自動フォーマットされるので書き終わった際には自動フォーマットすることを習慣づけてください。
- 「IOがある」ということを型で表すために`async` / `await`ではなくIOエラーから来るResult型を利用しているため、大概の **(実行を伴う)** 関数でResult型を返すようにしています。エラー処理は面倒くさいので、`?`演算子を多用してほぼ握りつぶしのように扱います。
- Option型が返ってくる場合でも、それがエラーによるもの(つまり受け付けられない入力)であるならば、`.ok_or`を使ってResult型に変更します。
- IOを明確にしたいため`println!`は禁止にします。デバッグ目的であれば`dbg!`を、出力であれば`print`を使ってください。`println!`特有のフォーマットがしたい場合は代わりに`format!`を使ってください。

## コーディング以外に関するルール

- コミットメッセージとPull Requestは日本語でお願いします。別に堅苦しい言葉遣いで書かなくていいです。
- Pull RequestやIssueでは議論内容に沿った話のみにするよう意識してください。書き方はラフで良いです。