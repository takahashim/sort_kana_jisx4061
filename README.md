# SortKanaJisx4061

Sort Japanese Kana strings by [JIS X 4061 (日本語文字列照合順番)](http://kikakurui.com/x4/X4061-1996-01.html) order in Ruby.

## Usage

```
require 'sort_kana_jisx4061'

words = [
  { original: '春', yomi: 'ハル' },
  { original: '夏', yomi: 'ナツ' },
  { original: '秋', yomi: 'アキ' },
  { original: '冬', yomi: 'フユ' },
]

words_sorted = sort_kana_jisx4061_by(words) {|x| x[:yomi] }
# => [{:original=>"秋", :yomi=>"アキ"}, {:original=>"夏", :yomi=>"ナツ"}, {:original=>"春", :yomi=>"ハル"}, {:original=>"冬", :yomi=>"フユ"}]
```

## Note

* Strings are exptected to be UTF-8
* Sorting Kanji is not supported
* Hiragana is converted to Katakana internally

## License

This software is released under the MIT License, see LICENSE.txt.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/emasaka/sort_kana_jisx4061 .
