# railsで頻出頻度が高いメソッドと使用例

'''link_to "表示名", URL(パス), class: "btn"'''
# => <a href="URL" class="btn">表示名</a>
# URLの部分は直接文字列を書いてもOK。user_pathなどの_pathメソッドを書いてもOK。
# @userのようにモデルのインスタンスも渡すことができる。（urlに:idなどを含む時に有用）
