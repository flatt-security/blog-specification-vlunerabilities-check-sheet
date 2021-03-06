# ファイルアップロード機能観点チェックリスト

## アイコンや写真のファイルアップロード

- [ ] ファイルの拡張子チェックがサーバーサイドで行われている
- [ ] ファイル拡張子のチェックを正規表現による後方一致、または言語ごとの関数を利用して末尾の拡張子をチェックするようなやり方で行っている
- [ ] 利用できるファイル形式を制限している
- [ ] 許可する拡張子を「許可リスト方式」で確認している
- [ ] ユーザーから送信された拡張子と実際のファイル形式を示すマジックナンバーが一致しているかを確認している
- [ ] ファイル名にディレクトリを示す文字列(`/`,`\`,`:`)が使われている場合に取り除いている、もしくは別の文字列に置き換えている
- [ ] 受け付けるファイルサイズを制限している
- [ ] ファイル名に個人情報が含まれないように変更している
- [ ] EXIF情報を削除している

## 業務データのCSV Bulk Import

- [ ] 入力された値がアプリケーションの仕様にとって望ましいものかどうかチェックしている
- [ ] 特殊記号 `=/+/-/@/Tab(0x09)/改行コード(\n,\r)/フィールド区切り文字(;/,)` が先頭に来ないようにしている

## 本人確認書類のアップロード

- [ ] 不要なデータは削除する仕組みが導入されている
- [ ] アップロードされたファイルにたいして適切なアクセス制限が行われている
- [ ] ファイル名の推測を困難にしている