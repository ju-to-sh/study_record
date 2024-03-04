## railsで頻出頻度が高いメソッドと使用例
### link_to
```
link_to "表示名", URL(パス), class: "btn"
# => <a href="URL" class="btn">表示名</a>

実例１
<%= link_to t('header.logout'), logout_path, class: 'dropdown-item', data: {turbo_method: :delete } %>

実例２
<%= link_to '#', class: 'nav-link', data: { bs_toggle: 'dropdown' }, aria: { haspopup: 'true', expanded: 'false' }, id: 'header-profile' do %>
  <%= image_tag('sample.jpg', size: '40x40', class: 'rounded-circle mr15')%>
<% end %>
```
- URLの部分は直接文字列を書いてもOK。user_pathなどの_pathメソッドを書いてもOK。
- @userのようにモデルのインスタンスも渡すことができる。（urlに:idなどを含む時に有用）
- 実例１の表示名の箇所は、tメソッド（I18n（国際化）テキストを翻訳するためのショートカット）を使用。rails7でDELETEメソッドのリクエストを送信する際は、data: {turbo_method: :delete }が必要。
- ブロックで記載することで画像やアイコンのタグを記載することができる。
