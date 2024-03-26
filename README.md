# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？

（💡リポジトリ…ファイルやディレクトリの状態を記録する場所＝ソースコードを置く場所 ）

+ **リモートリポジトリとは…インターネット上にあるソースコード置き場**  
→ 自分の作業内容を他の人に確認してもらったり、他の人の作業内容を取得したりできる
（代表的なサービス：Git Hub）

* **ローカルリポジトリとは…作業者の各PC上にあるソースコード置き場**  
→ 自分のPCで作業する時に利用するリポジトリで、変更履歴を管理しながら作業を行うことができる

## プッシュとマージの違いは何でしょうか？

+ **プッシュとは…ローカルリポジトリとリモートリポジトリ間で行う操作**  
→ ローカルリポジトリからリモートリポジトリへ、変更履歴を反映させることを「プッシュ」と呼ぶ
（リモートリポジトリからローカルリポジトリへの履歴の反映は「プル」と呼ぶ）

* **マージとは…各リポジトリのブランチ間で行う操作**  
→ 分岐したブランチでの変更履歴を別のブランチに取り込むことを「マージ」と呼ぶ

## コミットとプッシュの違い

+ **コミットとは…変更したファイルをローカルリポジトリに登録すること**  
→ 「ファイルを編集・変更 → add → commit」の順でGit（ローカルリポジトリ）に変更履歴を記録する

* **プッシュとは…コミット（登録）した変更を、ローカルリポジトリからリモートリポジトリへ反映させること**  
→ ファイルや変更履歴がアップロードされるため、バックアップにもなる

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？

+ **一目で変更内容がわかる**  
→「何を」「どう」変更したのか、具体的に書く

* **誰が読んでも内容が伝わる**  
→ 複雑な表現・言い回しは避け、簡潔に書く

+ **Prifixを用いて書く**  
→「Prifix」とは、コミットメッセージの先頭に特定の文字を付けること  
→ 何に対する変更なのか見やすくなる  
（例：「feat:タイトルロゴを更新」「fix:〇〇のエラーが起きているため、△△を修正」など）

## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？

+ **ローカルでマージするフロー…一人で行えるため、バグがあっても気づかない可能性がある**  
→ 全て自分のPC上で行えるため、コードにバグがあっても気づかずそのまま本番環境にアップされてしまう可能性がある

* **プルリクエストでマージするフロー…レビュワーを通して行うため、バグの発生を抑えられる**  
→ レビュワーにコードレビューをしてもらってからマージする手順になるため、事前にバグを発見できる


## コンフリクトを起こしてしまった場合、どう対処すべきですか？

+ **コンフリクトが起きている箇所を確認する**  
→ マージした際にメッセージが表示され、コンフリクトが起きている部分がわかる
（ファイルにもコンフリクトしている部分がわかるように変更が入る）

* **手動でファイルを修正する**  
→ 複数人で開発を行っている場合、他の人のソースコードの内容を把握する必要がでてくる  
→ もし、わからない・意図が読めない処理があった時は、そのコードを書いた本人と相談しながら修正を行うと良い

+ **コミットする**  
→ コンフリクトを解消してもマージは未完了のまま  
→ コミットすることでマージが完了する