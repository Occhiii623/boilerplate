---
title: はじめての記事
date: 2019-06-19
tags: ["サンプル", "チュートリアル"]
excerpt: これは抜粋です。
---

### hello world!

rubyプログラム

```ruby
def extra_end(str)
  char_num = str.length
  right2 = str.slice!(char_num - 2, 2)
  # 5文字数から3文字分削除して、第2引数で取り出す文字数を指定する
  puts right2*3
end

extra_end('Hello')
```