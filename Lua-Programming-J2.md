wikibooks
https://en.m.wikibooks.org/wiki/Lua_Programming

# Lua Programming

GNU Lesser General Public License
GNU Free Documentation License
GNU GENERAL PUBLIC LICENSE



# Introduction

Lua（「LUA」という表記は正しくありません）は、強力で、高速で、軽量で、埋め込み可能なプログラミング言語です。多くのフレームワーク、ゲーム、その他のアプリケーションで使用されています。単独で使用することもできますが、他のアプリケーションに簡単に組み込むことができるように設計されています。これは、非常に移植性の高いCプログラミング言語のサブセットであるANSI Cで実装されています。つまり、他のほとんどのスクリプト言語では実行できない多くのシステムやデバイスで実行できます。この本の目的は、以前のプログラミング経験に関係なく、誰にでもLuaプログラミングを教えることです。この本は、プログラミングの紹介として、これまでプログラミングしたことがない人のために、またはLuaの紹介として、他の言語でのプログラミング経験のある人のために使用できます。Luaを使用する開発プラットフォームやゲームはたくさんあるので、この本はLuaの使い方を学び、その開発プラットフォームでそれを使用するためにも使用できます。

この本は、Luaの最新バージョンの使用法を教えることを目的としています。これは、Luaの新しいバージョンがリリースされると、定期的に更新が試みられることを意味します（Luaのリリースはそれほど頻繁ではないため、それほど難しくはありません）。現在、この本は以前のバージョンであるLua5.2の最新版です。5.xブランチ（Lua5.0およびLua5.1）で古いバージョンのLuaを使用する組み込み環境でLuaを使用している場合でも、資料は十分に関連しているはずです。

Luaは、リオデジャネイロのポンティフィカルカトリック大学の研究所で設計および保守されています。作成者は、 Roberto Ierusalimschy、Waldemar Celes 、Luiz Henrique de Figueiredoです。



> 「ルア」（LOO-ahと発音）はポルトガル語で「月」を意味します。そのため、頭字語でも略語でもありませんが、名詞です。より具体的には、「ルア」は名前、地球の月の名前、そして言語の名前です。ほとんどの名前と同様に、小文字で最初の大文字、つまり「Lua」を使用して記述する必要があります。ひどくて紛らわしい「LUA」とは書かないでください。人によって意味が異なる略語になります。だから、ぜひ「Lua」と書くようにしてくださいね！
>
> —Luaの作者、[Luaについて](http://www.lua.org/about.html)

Luaは、TeCGraf（リオデジャネイロのポンティフィカルカトリック大学の研究所）によって設計された2つの言語、DELとSolに由来します。 DELは「データ入力言語」を意味し、Solは「単純なオブジェクト言語」を意味し、ポルトガル語で太陽も意味します。そのため、ポルトガル語で「月」を意味するため、Luaという名前が選ばれました。ブラジルの石油会社であるPetrobrasのために作成されましたが、TeCGrafの他の多くのプロジェクトでも使用され、現在では世界中の多数のプロジェクトで使用されています。 Luaは、組み込みゲーム開発の分野における主要な言語の1つです。

Luaの主な利点の1つは、そのシンプルさです。一部の企業は、その利点のためだけにそれを使用しています。プログラミング言語を使用して特定のタスクを実行できれば、従業員はよりよく働くことができると考えていますが、複雑なプログラミング言語のフルコースを従業員に提供する余裕はありません。ここでのBashやBatchのようないくつかの非常に単純な言語は、これらのタスクを実行するのに十分強力ではありませんが、Luaは強力で単純です。 Luaのもう1つの重要な利点は、組み込み機能です。これは、開発全体を通じて最も重要な特性の1つでした。 World of WarcraftやROBLOXのようなゲームは、ユーザーが使用できるように、アプリケーションにLuaを埋め込むことができる必要があります。

プログラミングは、組み込みアプリケーション内で実行されるプログラムの場合はスクリプトとも呼ばれ、コンピュータープログラムを作成するプロセスです。プログラミング言語は、コンピュータープログラムに含まれているコンピューターコードを介してコンピューターに指示を与えるために使用される言語です。プログラミング言語は、英語の文法に似た構文と、言語で提供される基本関数であるライブラリの2つで構成されています。これらのライブラリは、英語の語彙と比較できます。



## Hello, world

Luaは、アプリケーションに埋め込まれて使用することも、単独で使用することもできます。この本では、Luaをコンピューターにインストールするプロセスについては説明していませんが、[codepad](http://codepad.org/)または[the Lua demo](http://www.lua.org/demo.html)を使用してコードを実行できます。この本のLuaコードの最初の例は、基本的で伝統的な「hello world」プログラムです。

> **「Hello World」のプログラムは、**表示装置に「Hello world」出力するコンピュータプログラムです。これは通常、ほとんどのプログラミング言語で可能な最も単純なプログラムの1つであるため、プログラミング言語の最も基本的な構文を初心者に説明したり、言語またはシステムが正しく動作していることを確認したりするためによく使用されます。
>
> —ウィキペディア、[Hello world program](https://en.wikipedia.org/wiki/Hello_world_program)



```lua
print("Hello, world!")
```

上記のコードは、Hello, world! というテキストを出力します。紙に何かを印刷するのではなく、出力にテキストを表示することを参照してプリントします。これは、`print`という関数を呼び出すことによって引数として文字列"Hello, world!"を使用して行われます。これについては、関数に関する章で説明します。

Luaはほとんどの場合、低レベルのアプリケーションに[埋め込まれ](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Embedded_system&usg=ALkJrhjO7IDN0JceQxPpd_cx_j0Qs56Ktg)ていることに注意してください。つまり、`print`関数は、ユーザーに表示される領域にテキストを常に表示するとは限りません。これらのアプリケーションのプログラミングインターフェイスのドキュメントでは、一般に、テキストをユーザーに表示する方法について説明します。



## Comments

コメントとは、プログラミング言語によって無視されるコード注釈です。コメントは、1行または複数行のコードの説明、プログラムの文書化、コードの一時的な無効化、またはその他の理由で使用できます。Luaがコメントだと認識できるようにするには、接頭辞として2つのハイフン`--`を付ける必要があり、独自の行または別の行の末尾に配置できます。



```lua
print("This is normal code.")
-- This is a comment
print("This is still normal code.") -- This is a comment at the end of a line of code.
```

これらのコメントはショートコメントと呼ばれます。長い括弧`--[[`で始まり、多くの行に続く長いコメントを作成することもできます。


```lua
print("This is normal code")
--[[Line 1
Line 2
]]
```

長い角かっこは2つの角かっこ `[[ ` で 構成され、その中央に任意の数の等号 `=`を付けることができます。その等号の数は、長い括弧のレベルと呼ばれます。長い角かっこは、同じレベルの次の角かっこがあるところまで続きます。等号のない長い角かっこは、レベル0の長い角かっこと呼ばれます。このアプローチでは、2つの角かっこの中央に等号を追加することにより、長いコメントの内側で閉じている二重角かっこを使用できます。コメントを使用してコードのブロックを無効にする場合は、これを行うと便利なことがよくあります。



```lua
--[==[
This is a comment that contains a closing long bracket of level 0 which is here: ]]
However, the closing double bracket doesn't make the comment end, because the comment was opened with an opening long bracket of level 2, and only a closing long bracket of level 2 can close it.
]==]
```

上記の例では、レベル0の閉じている長い括弧（`]]`）はコメントを閉じませんが、レベル2の閉じている長い括弧（`]==]`）で閉じます。



## Syntax

プログラミング言語の構文は、文法が文や単語の書き方を定義するのと同じように、ステートメントや式をそのプログラミング言語で書く方法を定義します。文と表現はそれぞれ文と単語と比較することができます。式は、値を持ち、評価できるコードの断片です。一方、ステートメントは、実行可能で、命令とその命令を使用する1つまたは複数の式を含むコードの断片です。たとえば、`3 + 5`は式であり、`variable = 3 + 5` はその式の値を変数に設定するステートメントです。

Luaの構文全体は、[Lua Webサイト](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=http://www.lua.org/manual/5.1/manual.html&usg=ALkJrhj_HxYENqimSypV-FZTjPomzfmbbA#8)の拡張バッカスナウア記法で見つけることができますが、それを読んでも何も理解できません。[拡張バッカスナウア記法](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_Form&usg=ALkJrhhZ5MEl-WEm6LiP6u5gH88OH4qsCg)はメタ言語であり、メタウェブサイトがウェブサイトに関するウェブサイトであるように、別の言語を説明するために使用される言語であり、Luaではメタテーブルが他のテーブルの動作を定義するテーブルです（この本の後半のメタテーブルとテーブルについてで学習します）。ただし、この本では、拡張バッカスナウア記法を学ぶ必要はありません。Luaのような言語はメタ言語を使用して説明できますが、単語や文を使用して英語で説明することもできます。これはまさに、この本がしていることです。

英語は別の言語を説明するために使用できるため、それ自体がメタ言語である必要があります（メタ言語の定義に対応しているため）。これは確かに事実です。また、プログラミング言語の目的は命令を記述することであり、英語でそれを行うことができるため、英語もプログラミング言語である必要があります。これは**、ある意味で**、そうです。実際、英語は多くのことに使用できる言語です。ただし、拡張バッカスナウア記法は特殊言語であり、プログラミング言語も特殊言語です。専門化は、特定のことを行うのは非常に得意であるが、他のことを行うことができないという特徴です。拡張バッカスナウア記法は他の言語の記述に非常に優れていますが、指示を書いたりメッセージを伝えたりするために使用することはできません。プログラミング言語は指示を与えるのに非常に優れていますが、言語の記述やメッセージの伝達には使用できません。

英語は、言語の説明、指示の提供、メッセージの伝達など、すべてを行うことができます。しかし、プログラミング言語と同等のことはあまり得意ではありません。実際、英語では指示を与えるのは非常に苦手なので、コンピューターに指示を与えるために使用された場合、コンピューターは何も理解しません。これは、コンピューターが非常に正確で明確な指示を必要とするためです。



## Obtaining Lua

Luaは、Luaの公式Webサイトの[ダウンロードページ](http://www.lua.org/download.html)から入手できます。手順もそこにあります。ダウンロードボタンはソースコード用ですが、おそらくあなたが望むものではありません。おそらくバイナリを探しているので、ページを見てそれらに関する情報を見つける必要があります（使用しているプラットフォームによって異なります）。この本の目的は、Lua言語を教えることだけであり、Luaツールの使用法を教えることではありません。この本では読者は組み込み環境でLuaを使用すると想定れていますが、必ずしもそのとおりであるわけではありません。それは、この本の中では、Luaの使用法をスタンドアロン言語として説明していないことを意味するだけです。 



## Quiz

この章の内容を理解したことを確認するために質問がいくつかあります。これらの質問の対する答えを見つけるには、この章に記載されていない知識が必要になる場合があることに注意してださい。これは正常なことです。クイズは学習体験の一部であり、本の他の場所では入手できない情報を紹介することができます。



**1**　ポルトガル語で「Lua」とはどういう意味ですか？



**2**　レベル0の長いコメントはどれですか？

|      | 選択肢             |
| ---- | ------------------ |
|      | `--Comment `       |
|      | `[[Comment]] `     |
|      | `--[[Comment]] `   |
|      | `--[=[Comment]=] ` |
|      | `[=[Comment]=] `   |

**3**　拡張バッカスナウア記法とは何ですか？

|      | 選択肢                           |
| ---- | -------------------------------- |
|      | A language                       |
|      | A programming language           |
|      | A natural (or ordinary) language |
|      | A notation                       |
|      | A metalanguage                   |
|      | A markup language                |

# Expressions

前に説明したように、式は値を持ち、評価できるコードの断片です。これらは（関数呼び出しを除いて）直接実行できないため、式で構成される次のコードのみを含むスクリプトはエラーになります。



```lua
3 + 5
-- The code above is erroneous because all it contains is an expression.
-- The computer cannot execute '3 + 5', since that does not make sense.
```

コードは一連のステートメントで構成されている必要があります。これらのステートメントには、ステートメントが命令を実行するために操作または使用する必要のある値となる式を含めることができます。

この章の一部のコード例は、式のみで構成されているため、有効なコードを構成していません。次の章では、ステートメントについて説明し、有効なコードの記述を開始できるようにします。



## Types

式を評価することは、式を計算してその値を見つけることです。特定の式が評価する値は、環境とスタックレベルに依存する可能性があるため、コンテキストごとに異なる場合があります。この値は、数値、テキスト、その他の多くのデータ型のいずれかになる場合があります。そのため、型があると言われます。

Luaおよび一般的なプログラミングでは、式は通常、0個以上の演算子を持つ1つ以上の値で構成されます。一部の演算子は、一部のタイプでのみ使用できます（たとえば、テキストを分割しようとするのは非論理的ですが、数値を分割することは理にかなっています）。演算子には、単項演算子と二項演算子の2種類があります。単項演算子は、1つの値のみを取る演算子です。たとえば、単項演算子は、パラメータとして-5、-3、-6などの1つの数値のみを取ります。パラメータとして1つの数値を取り、その数値を無効にします。ただし、同じ演算子ではない2項演算子は、2つの値を取り、最初の値から2番目の値を減算します：5-3、8-6、4-9など。



`type`関数を使用して、数値の型を文字列として取得することができます。



```lua
print(type(32425)) --> number
```

### Numbers

数字は一般的に数量を表しますが、他の多くのことに使用できます。Luaの数値型は、実数とほとんど同じように機能します。数値は、整数、10進数、10進数の指数、または[16進数](https://en.wikipedia.org/wiki/hexadecimal)で構成できます。有効な番号は次のとおりです。



- 3
- 3.0
- 3.1416
- 314.16e-2
- 0.31416E1
- 0xff
- 0x56

#### Arithmetic operations

Luaの数値の演算子は次のとおりです。

The operators for numbers in Lua are the following:

| 操作         | 構文   | 説明                                         | 例        |
| ------------ | ------ | -------------------------------------------- | --------- |
| 算術否定     | -a     | aの符号を変更し、値を返します                | -3.14159  |
| 添加         | a + b  | aとbの合計を返します                         | 5.2 + 3.6 |
| 減算         | a-b    | aからbを減算し、結果を返します               | 6.7 - 1.2 |
| 乗算         | a * b  | aとbの積を返します                           | 3.2 * 1.5 |
| べき乗       | a ^ b  | aをbの累乗、またはaのbによるべき乗に返します | 5 ^ 2     |
| 分割         | a / b  | aをbで除算し、結果を返します                 | 6.4 / 2   |
| モジュロ演算 | a ％ b | aをbで割った余りを返します                   | 5 % 3     |

最後のものを除いて、これらの演算子（基本的な数学演算子と同じ）はすべてすでに知っているでしょう。最後のものはモジュロ演算子と呼ばれ、ある数値を別の数値で除算した余りを単純に計算します。たとえば、5％3は、2が5を3で割った余りであるため、結果として2になります。モジュロ演算子は他の演算子ほど一般的ではありませんが、複数の用途があります。

You probably already know all of these operators (they are the same as basic mathematical operators) except the last. The last is called the modulo operator, and simply calculates the remainder of the division of one number by another. 5 % 3, for example, would give 2 as a result because 2 is the remainder of the division of 5 by 3. The modulo operator is less common than the other operators, but it has multiple uses.

#### Integers

数値の新しいサブタイプである整数がLua5.3で追加されました。数値は整数または浮動小数点数のいずれかです。浮動小数点数は上記の数値に似ていますが、整数は小数部のない数値です。浮動小数点の除算（`/`）とべき乗は、常にオペランドを浮動小数点数に変換しますが、他のすべての演算子は、2つのオペランドが整数の場合、整数を返します。その他の場合、フロア分割演算子（`//`）を除いて、結果はフロートになります。



### Nil

Nilは値 nilのタイプであり、その主なプロパティは他の値とは異なります。これは通常、有用な値がないことを表します。nilを値に持つものの例：

Nil is the type of the value nil, whose main property is to be different from any other value; it usually represents the absence of a useful value. Some examples of things that have the value nil:

- 値を割り当てる前にアクセスする変数の値
- スコープ外の変数にアクセスしようとしたときに取得する値
- 割り当てられていないテーブル内のキーの値
- `tonumber`によって文字列を数値に変換できない場合に返される値


より高度な注意点として、意図的にnil値を割り当てると、変数またはテーブルへの参照が削除され、[ガベージコレクター](https://en.m.wikibooks.org/w/index.php?title=Garbage_collection&action=edit&redlink=1)がそのメモリを再利用できるようになります。



### Booleans

ブール値は true または false のいずれかになりますが、それ以外はありません。これは、予約キーワードである`true`と`false`としてLuaで記述されています。注意すべき重要な点は、これは前述`nil`のように異なるデータ型であるということです。`and`、`or`、`not()`　は通常ブール値と関連していますが、Luaの任意のデータ型で使用することができます。



| 操作       | 構文     | 説明                                                         |
| ---------- | -------- | ------------------------------------------------------------ |
| ブール否定 | not a    | aがfalseまたはnilの場合、trueを返します。それ以外の場合は、falseを返します。 |
| 論理積     | a and  b | falseまたはnilの場合、最初の引数を返します。それ以外の場合は、2番目の引数を返します。 |
| 論理和     | a or  b  | falseでもnilでもない場合、最初の引数を返します。それ以外の場合は、2番目の引数を返します。 |

基本的に、`not`演算子はブール値を否定するだけで（trueの場合はfalseにし、falseの場合はtrueにします）、`and`演算子は両方がtrueの場合はtrueを返し、そうでない場合はfalseを返し、`or`演算子はいずれかの引数がtrueの場合はtrueを返します。それ以外の場合はfalse。ただし、上記の表で正確な動作方法が説明されているため、これは正確には動作しません。Luaでは、論理式では値falseとnilの両方がfalseと見なされ、その他はすべてtrueと見なされます（0と空の文字列も含む）。

次の章で紹介する関係演算子（`<`、`>`、`<=`、`>=`、`~=`、`==`）は必ずしもオペランドとしてブール値を取ることはありませんが、常に結果としてブール値が得られます。

これを調整するのは難しい場合があります。わかりやすくするために、ここにいくつかの真理値表または式と結果のペアを示します。ここで`x`は`nil`、`true`または`false`：



| 式            | 結果    |
| ------------- | ------- |
| `true and x`  | `x`     |
| `false and x` | `false` |
| `nil and x`   | `nil`   |
|               |         |
| `true or x`   | `true`  |
| `false or x`  | `x`     |
| `nil or x`    | `x`     |

これはやや直感に反することを意味します

| 式              | 結果    |
| --------------- | ------- |
| `false and nil` | `false` |
| `nil and false` | `nil`   |

加えて

| 式                            | 結果    |
| ----------------------------- | ------- |
| `false == nil` `nil == false` | `false` |
| `nil and false`               | `nil`   |

| 式                      | 結果    |
| ----------------------- | ------- |
| `not(false)` `not(nil)` | `true ` |
| `not(true)`             | `false` |

### Strings

文字列は、テキストを表すために使用できる文字のシーケンスです。これらは、[コメントに関するセクションで]()前に説明した二重引用符、一重引用符、または長い角かっこで囲むことにより、Luaで記述でき[ます。コメントと文字列には、コメントの場合は2つのハイフンを前に付けて、両方を長い角かっこで区切ることができるという事実以外に共通点がないことに注意してください）。長い括弧に含まれていない文字列は、1行だけ続きます。このため、長い角かっこを使用せずに多くの行を含む文字列を作成する唯一の方法は、エスケープシーケンスを使用することです。これは、特定の場合に一重引用符または二重引用符を挿入する唯一の方法でもあります。エスケープシーケンスは、Luaでは常にエスケープ文字であるバックスラッシュ（ ' \ ' ）と、エスケープする文字を識別する識別子の2つで構成されます。



| Escape sequence | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| \n              | 改行                                                         |
| \"              | 二重引用符（ダブルクォーツ）                                 |
| \'              | 一重引用符（またはアポストロフィ）                           |
| \\              | バックスラッシュ                                             |
| \t              | 水平tab                                                      |
| \###            | ０から255 までの数字でなければなりません。結果は対応する [ASCII文字](https://en.wikipedia.org/wiki/ASCII) . |

文字を文字列に直接入れると問題が発生する場合は、エスケープシーケンスを使用します。たとえば、二重引用符で囲まれ、二重引用符を含める必要があるテキストの文字列がある場合は、文字列を別の文字で囲むか、二重引用符をエスケープする必要があります。長い角かっこで区切られた文字列内の文字をエスケープする必要はありません。これはすべての文字に当てはまります。長い括弧で区切られた文字列内のすべての文字は、そのまま使用されます。`%` 文字は、魔法の文字をエスケープする文字列パターンで使用されていますが、用語のエスケープは、別のコンテキストで使用されています。



```lua
"This is a valid string."

'This is also a valid string.'

"This is a valid \" string 'that contains unescaped single quotes and escaped double quotes."

[[
This is a line that can continue
on more than one line.

It can contain single quotes, double quotes and everything else (-- including comments). It ignores everything (including escape characters) except closing long brackets of the same level as the opening long bracket.
]]

"This is a valid string that contains tabs \t, double quotes \" and backlashes \\"

"This is " not a valid string because there is an unescaped double quote in the middle of it."
```

便宜上、開いている長い文字列ブラケットの直後に新しい行が続く場合、その新しい行は無視されます。したがって、次の2つの文字列は同等です。



```lua
[[This is a string
that can continue on many lines.]]

[[
This is a string
that can continue on many lines.]]

-- Since the opening long bracket of the second string is immediately followed by a new line, that new line is ignored.
```

単項長演算子 ( '＃' )を使用すると、文字列の長さを数値として取得できます。



```lua
print(#("This is a string")) --> 16
```

#### Concatenation

[形式言語理論](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/formal_language&usg=ALkJrhhiq47ZaA189c8B3lAkhbdIPf-fsw)と[コンピュータプログラミング](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/computer_programming&usg=ALkJrhh0AyYC55lQ-sU28Pv_ZemrP7dAUQ)、**文字列の連結は、** 2つの[文字列](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/character_string_(computer_science)&usg=ALkJrhi_O9cTd4GHux39enA4M1-llG5B1w)エンドツーエンドをつなげる操作です。たとえば、「雪」と「ボール」の連結は「雪玉」です。

—ウィキペディア、 [Concatenation](https://en.wikipedia.org/wiki/Concatenation)

> In [formal language theory](https://en.wikipedia.org/wiki/formal_language) and [computer programming](https://en.wikipedia.org/wiki/computer_programming), **string concatenation** is the operation of joining two [character strings](https://en.wikipedia.org/wiki/character_string_(computer_science)) end-to-end. For example, the concatenation of "snow" and "ball" is "snowball".
>
> —Wikipedia, [Concatenation](https://en.wikipedia.org/wiki/Concatenation)

Luaの文字列連結演算子は、2つのドット ('..') で示されます。これは、「snow」と「ball」を連結して結果を出力する連結の例です。



```lua
print("snow" .. "ball") --> snowball
```

このコードは「snow」と「ball」を連結し、結果を出力します。



### Other types

Luaの4つの基本タイプ（数値、ブール値、nil、文字列）については前のセクションで説明しましたが、関数、テーブル、ユーザーデータ、スレッドの4つのタイプがありません。関数は、呼び出して値を受け取り、値を返すことができるコードの断片です。テーブルは、データ操作に使用できるデータ構造です。ユーザーデータは、Luaが組み込まれているアプリケーションによって内部的に使用され、Luaがアプリケーションによって制御されるオブジェクトを介してそのプログラムと通信できるようにします。最後に、スレッドはコルーチンによって使用されます。これにより、多くの関数を同時に実行できます。これらはすべて後で説明するので、他のデータ型があることだけを覚えておいてください。



## Literals

リテラルは、ソースコードで固定値を表すための表記法です。Luaではスレッドとユーザーデータを除くすべての値は、リテラルとして表すことができます。文字列リテラル（文字列として評価されるリテラル）は、たとえば、テキストの文字列を一重引用符、二重引用符、または長い角かっこで囲んで構成します。一方、数値リテラルは、10進表記（例: `12.43`)、科学的記数法（例：`3.1416e-2`および`0.31416E1`）、または16進表記（例:`0xff`)を使用して表現された数値で構成されます。



## Coercion

Coercion とは、あるデータ型の値を別のデータ型の値に変換することです。Luaは、文字列値と数値の間の自動変換を提供します。文字列に適用される算術演算は、この文字列を数値に変換しようとします。逆に、文字列が予期され、代わりに数値が使用される場合は常に、数値は文字列に変換されます。これは、Lua演算子とデフォルト関数（言語で提供される関数）の両方に適用されます。



```lua
print("122" + 1) --> 123
print("The number is " .. 5 .. ".") --> The number is 5.
```

数値から文字列への Coercion および文字列から数値への Coercion は、`tostring` 関数と 　`tonumber` 関数を使用して手動で行うこともできます。前者は数値を引数として受け入れて文字列に変換し、後者は文字列を引数として受け入れて数値に変換します（デフォルトの10進数とは異なるベースをオプションで2番目の引数に指定できます）。



## Bitwise operations

Lua 5.3以降、2進数（ビットパターン）を操作するためのビット演算子が提供されています。これらの演算子は他の演算子ほど頻繁には使用されないため、不要な場合はこのセクションをスキップできます。

Luaのビット演算子は常に整数を操作し、必要に応じてオペランドを変換します。それらは整数も与えます。

ビット単位のAND演算（演算子`&`を使用）は、同じ長さの2つのバイナリ表現のビットの各ペアに対して論理積を実行します。たとえば、`5 & 3` は 1 と評価されます。これは、これらの数値の2進表現を調べることで説明できます（下付き文字は基数を示すために使用されます）。



![(5)_{{10}}=(0101)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7d7304ba8f4097f07787270c75a4a8fee5558f3e)

![(3)_{{10}}=(0011)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/cc7e6d2c6b228674c5c57b9f82b086f0177e41d2)

![(1)_{{10}}=(0001)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7a6a4e17ea375c6c55f3bc5053bb8a17070c19f5)

5と3の両方のバイナリ表現の特定の位置にあるビットが1である場合（最後のビットの場合のように）、その位置にあるビットは1になります。それ以外の場合はすべて0になります。



ビット単位のOR演算（演算子`|`を使用）は、ビット単位のAND演算と同じように機能し、論理積を実行する代わりに論理和を実行します。したがって、`5 | 3` は7と評価されます。



![(5)_{{10}}=(0101)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7d7304ba8f4097f07787270c75a4a8fee5558f3e)

![(3)_{{10}}=(0011)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/cc7e6d2c6b228674c5c57b9f82b086f0177e41d2)

![(7)_{{10}}=(0111)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/e3e15c3c8aa9d76b66bb3a556f837dd3b85905a2)

ここで、2つのオペランドのバイナリ表現がその位置に0ビットを持っていた場合にのみ、最終結果の各位置のビットが0であることがわかります。



ビット単位のXOR演算（演算子`~`を使用）は他の2つの演算と同じように機能しますが、特定の位置では、オペランドのビットの両方ではなく片方が1の場合、最後のビットは1になります。



![(5)_{{10}}=(0101)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7d7304ba8f4097f07787270c75a4a8fee5558f3e)

![(3)_{{10}}=(0011)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/cc7e6d2c6b228674c5c57b9f82b086f0177e41d2)

![(6)_{{10}}=(0110)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/fc5e1e2283de38017ad922d2605016d653b6d436)

これは前の例と同じですが、両方のオペランドの最後のビットが1であったため、結果の最後のビットが1ではなく0であることがわかります。



ビット単位のNOT演算（演算子`~`を使用）は、一意のオペランドの各ビットに対して論理否定を実行します。つまり、0が1になり、1が0になります。したがって、`~7` は -8 と評価されます。



![(7)_{{10}}=(0111)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/e3e15c3c8aa9d76b66bb3a556f837dd3b85905a2)

![(8)_{{10}}=(1000)_{2}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c146e6bd4e3cba0908fea6a819b278a46c3bffc7)

ここで、最初のビットはオペランドが0であるため結果で1になり、他のビットはすべて1であるため0になります。



[![Left shift](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Rotate_left_logically.svg/210px-Rotate_left_logically.svg.png)](https://en.m.wikibooks.org/wiki/File:Rotate_left_logically.svg)[![Right shift](https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/Rotate_right_arithmetically.svg/175px-Rotate_right_arithmetically.svg.png)](https://en.m.wikibooks.org/wiki/File:Rotate_right_arithmetically.svg)

これらのビット演算子に加えて、Lua5.3は算術ビットシフトもサポートしています。演算子`<<`を使用して左側に示されている左シフトは、すべてのビットを、第2オペランドに対応するビット数だけ左にシフトすることで構成されます。演算子で示され、右に示されている右シフト`>>`も同じですが、反対方向です。



## Operator precedence

演算子の優先順位は、Luaでも数学で通常行われるのと同じように機能します。特定の演算子は他の演算子よりも先に評価され、括弧を使用して、操作を実行する順序を任意に変更できます。演算子が評価される優先度は、優先度の高いものから低いものへと、以下のリストにあります。これらの演算子のいくつかはまだ議論されていませんが、それらはすべてこの本のある時点でカバーされます。



1. べき乗： `^`

2. 単項演算子：`not`、`#`、`-`、`~`

3. レベル2数学演算子：`*`、`/`、`//`、`%`

4. レベル1の数学演算子：`+`、`-`

5. 連結： `..`

6. ビットシフト：`<<`、`>>`

7. ビットごとのAND： `&`

8. ビットごとのXOR： `~`

9. ビットごとのOR： `|`

10. 関係演算子：`<`、`>`、`<=`、`>=`、`~=`、`==`

11. ブール値と： `and`

12. ブール値または： `or`

    

## Quiz

この章の内容を理解したことを確認するために回答できる質問がいくつかあります。これらの質問のいくつかに対する答えを見つけるには、この章に記載されていない知識が必要になる場合があることに注意してください。これは正常です。クイズは学習体験の一部であり、本の他の場所では入手できない情報を紹介することができます。



**1**　何が出力されますか？`print(type(type(5.2)))`



**2** `0 or 8` この式は何を返しますか？

|      | 選択肢   |
| ---- | -------- |
|      | `true `  |
|      | `false ` |
|      | `0 `     |
|      | `8 `     |

**3** どの文字列が有効ですか？

|      | 選択肢           |
| ---- | ---------------- |
|      | `"test's test"`  |
|      | `'test\'s test'` |
|      | `"test"s test"`  |
|      | `'test"s test'`  |
|      | `"test\'s test"` |
|      | `'test's test'`  |

**4** どの式が`"1223"`の文字列を与えますか？

|      | 選択肢        |
| ---- | ------------- |
|      | `"122" + 3`   |
|      | `"122" .. 3`  |
|      | `"12" + "23"` |
|      | `12 .. 23`    |

**5** 正誤問題 `not 5^3 == 5` true or false? 

|      | 選択肢  |
| ---- | ------- |
|      | `true`  |
|      | `false` |

#  Statements

ステートメントは、実行可能なコードの一部であり、ステートメントで使用する命令と式が含まれています。一部のステートメントには、たとえば特定の条件下で実行される可能性のあるコードも含まれます。式とは異なり、式に直接入れることができ、実行されます。Luaにはいくつかの命令がありますが、これらの命令を他の命令や複雑な式と組み合わせると、ユーザーに十分な制御と柔軟性が与えられます。



## Assignment

プログラマーは、後で使用できるように、値をメモリーに格納できる必要があることがよくあります。これは変数を使用して行われます。変数は、コンピューターのメモリに格納されている値への参照です。それらは、メモリに保存した後、後で番号にアクセスするために使用できます。割り当ては、変数に値を割り当てるために使用される命令です。これは、値を格納する必要がある変数の名前、等号、および変数に格納する必要がある値で構成されます。



```lua
variable = 43
print(variable) --> 43
```

上記のコードで示されているように、変数の値にアクセスするには、変数の名前を値にアクセスする必要があります。



### The assignment operator

Luaでは、他のほとんどのプログラミング言語と同様に、等号（`=`）は、右側のオペランドの式の値を左側のオペランドで指定された変数に割り当てる2項代入演算子として機能します



### Assignment of variables

次の例は、変数の割り当てに等号を使用する方法を示しています。



```lua
fruit = "apple"   -- assign a string to a variable
count = 5         -- assign a numeric value to a variable
```

### Strings and Numeric Values

リテラル文字列は、変数名と区別するために引用符で囲む必要があることに注意してください。



```lua
apples = 5
favourite = "apples"   -- without quotes, apples would be interpreted as a variable name
```

変数名は数字で始めることができないため、数値を引用符で囲む必要はなく、変数名として誤って解釈することはできないことに注意してください。



```lua
apples = 6    -- no quotes are necessary around a numeric parameter
pears = "5"   -- quotes will cause the value to be considered a string
```

### Multiple Assignments

Luaプログラミング言語は複数の割り当てをサポートしています。



```lua
apples, favorite = 5, "apples" -- assigns apples = 5, favorite = "apples"
```

### Identifiers

Luaでは、[識別子](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Identifier&usg=ALkJrhjOm8MkOYUvFRaGGawhC9zzFbfEew#In_computer_science)は名前とも呼ばれます。文字、数字、アンダースコアで構成され、数字で始まらない任意のテキストを使用できます。これらは、テーブルに関する章で説明する変数とテーブルフィールドに名前を付けるために使用されます



いくつかの有効な名前は次のとおりです。

- `name`
- `hello`
- `_`
- `_tomatoes`
- `me41`
- `__`
- `_thisIs_StillaValid23name`



いくつかの無効な名前は次のとおりです。

- `2hello` ：数字で始まる

- `th$i` ：文字、数字、またはアンダースコアではない文字が含まれている

- `hel!o` ：文字、数字、またはアンダースコアではない文字が含まれている

- `563text` ：数字で始まる

- `82_something` ：数字で始まる

- `2hello` : starts with a digit

- `th$i` : contains a character that isn't a letter, a digit or an underscore

- `hel!o` : contains a character that isn't a letter, a digit or an underscore

- `563text` : starts with a digit

- `82_something` : starts with a digit

  

また、次のキーワードのLUAによって予約されており、名称として使用することはできません：`and`、`end`、`in`、`repeat`、`break`、`false`、`local`、`return`、`do`、`for`、`nil`、`then`、`else`、`function`、`not`、`true`、`elseif`、`if`、`or`、`until`、`while`。



変数またはテーブルフィールドに名前を付けるときは、その有効な名前を選択する必要があります。したがって、文字またはアンダースコアで始まり、文字、アンダースコア、および数字のみを含める必要があります。Luaでは大文字と小文字が区別されることに注意してください。これは、`Hello`と`hello`が2つの異なる名前であることを意味します。



### Scope

[変数](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Scope_(computer_science)&usg=ALkJrhgPIty13LsluvhQl0GnViEF63s0ow)の[スコープ](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Scope_(computer_science)&usg=ALkJrhgPIty13LsluvhQl0GnViEF63s0ow)は、その変数が意味を持つプログラムのコードの領域です。これまでに見た変数の例はすべてグローバル変数の例であり、プログラムのどこからでもアクセスできる変数です。一方、ローカル変数は、それらが定義されたプログラムの領域から、およびプログラムのその領域内にあるプログラムの領域でのみ使用できます。これらはグローバル変数とまったく同じ方法で作成されますが、接頭辞として`local`キーワードを付ける必要があります。



`do`ステートメントは、それらを記述するために使用されます。この`do`ステートメントは、新しいコードブロック、つまり新しいスコープを作成する以外の目的がないステートメントです。`end`キーワードで終わります：



```lua
local variable = 13 -- This defines a local variable that can be accessed from anywhere in the script since it was defined in the main region.
do
	-- This statement creates a new block and also a new scope.
	variable = variable + 5 -- This adds 5 to the variable, which now equals 18.
	local variable = 17 -- This creates a variable with the same name as the previous variable, but this one is local to the scope created by the do statement.
	variable = variable - 1 -- This subtracts 1 from the local variable, which now equals 16.
	print(variable) --> 16
end
print(variable) --> 18
```

スコープが終了すると、スコープ内のすべての変数が削除されます。コードの領域では、含まれているコードの領域で定義された変数を使用できますが、同じ名前のローカル変数を定義して変数を「上書き」すると、コードの他の領域で定義された変数の代わりにそのローカル変数が使用されます。 。これが、print関数の最初の呼び出しが16を出力し、`do`ステートメントによって作成されたスコープ外の2番目の呼び出しが18を出力する理由です。



実際には、ローカル変数のみを使用する必要があります。ローカル変数は、グローバル変数のように現在の関数の環境に格納されるのではなく、レジスタに格納されるため、グローバル変数よりも高速に定義およびアクセスできるためです。レジスターは、Luaがローカル変数を格納してそれらにすばやくアクセスするために使用する領域であり、通常は最大200個のローカル変数しか含めることができません。すべてのコンピューターの重要なコンポーネントであるプロセッサーにもレジスターがありますが、これらはLuaのレジスターとは関係ありません。各関数（メインスレッド、プログラムのコア、関数でもある）にも独自の環境があります。これは、変数名にインデックスを使用し、これらの変数の値をこれらのインデックスに対応する値に格納するテーブルです。



### Forms of assignment

#### Augmented assignment

複合代入とも呼ばれる[拡張代入](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/augmented_assignment&usg=ALkJrhikuZjAdzs7U5ormJmVswQmKe2I2g)は、変数に前の値を基準にした値を与えるタイプの代入です。たとえば、現在の値をインクリメントする、aの値を8ずつインクリメントするコード`a += 8`相当するものは、[C](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/C_(programming_language)&usg=ALkJrhiCKRK36t_KSDoPF3Pn4cHeTdDEkg)、[JavaScript](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/JavaScript&usg=ALkJrhh7zVRtj4K3FtxX_r4i7EYhiSqtlw)、[Ruby](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Ruby_(programming_language)&usg=ALkJrhjzUGQdMGYRxbbFJVnabYKtQcLMTw)、[Python](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Python_(programming_language)&usg=ALkJrhhE0iY1VFHE7kYCrOh5VrK0LUblFQ)に存在しますが、Luaには存在しません。つまり、`a = a + 8` と記述する必要があります。



#### Chained assignment

[連鎖割り当て](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/chained_assignment&usg=ALkJrhgehEARyigOZsol5yhQc_EDmvGTNA)は、多くの変数に単一の値を与える割り当ての一種です。たとえば、このコード`a = b = c = d = 0`は、CおよびPythonでa、b、c、およびdの値を0に設定します。Luaでは、このコードはエラーを発生させるため、前の例は次のように記述する必要があります。



```lua
d = 0
c = d -- or c = 0
b = c -- or b = 0
a = b -- or a = 0
```

#### Parallel assignment

[並列割り当て](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/parallel_assignment&usg=ALkJrhjRq6OLEUV5Vz11i3F4GbHyYr19fg)は、同時割り当ておよび複数割り当てとも呼ばれ、異なる変数に異なる値（同じ値にすることもできます）を同時に割り当てるタイプの割り当てです。連鎖割り当てや拡張割り当てとは異なり、Luaでは並列割り当てを使用できます。

前のセクションの例は、並列割り当てを使用するように書き直すことができます。



```lua
a, b, c, d = 0, 0, 0, 0
```

値よりも多くの変数を指定すると、一部の変数には値が割り当てられません。変数よりも多くの値を指定すると、余分な値は無視されます。より技術的には、値のリストは、割り当てが行われる前に変数のリストの長さに調整されます。つまり、余分な値が削除され、最後に余分なnil値が追加されて、のリストと同じ長さになります。*変数値リストの最後*に関数呼び出しがある場合、関数呼び出しが括弧で囲まれていない限り、返される値はそのリストの最後に追加されます。



さらに、ほとんどのプログラミング言語とは異なり、Luaは[permutation （順列）](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/permutation&usg=ALkJrhhRb0PyUQ2b_i7Jt4_nA1LscYhbvQ)を介して変数の値の再割り当てを可能にします。例えば：



```lua
first_variable, second_variable = 54, 87
first_variable, second_variable = second_variable, first_variable
print(first_variable, second_variable) --> 87 54
```

これが機能するのは、割り当てステートメントが何かを割り当てる前にすべての変数と値を評価するためです。割り当ては、実際に同時であるかのように実行されます。つまり、新しい値が割り当てられる前に、変数とその変数の値でインデックス付けされたテーブルフィールドに同時に値を割り当てることができます。つまり、次のコードは、`dictionary[1]`を12に設定するのではなく`dictionary[2]`に設定します。



```lua
dictionary = {}
index = 2
index, dictionary[index] = index - 1, 12
```

## Conditional statement

条件文は、式が真であるかどうかをチェックし、真である場合は特定のコードを実行する命令です。式が真でない場合は、そのコードをスキップするだけで、プログラムが続行されます。Luaでは、唯一の条件文が`if`命令を使用します。Falseとnilは両方ともfalseと見なされ、その他はすべてtrueと見なされます。



```lua
local number = 6

if number < 10 then
	print("The number " .. number .. " is smaller than ten.")
end

-- Other code can be here and it will execute regardless of whether the code in the conditional statement executed.
```

上記のコードでは、変数番号には、代入ステートメントを使用して番号6が割り当てられています。次に、条件ステートメントは、変数番号に格納されている値が10より小さいかどうかをチェックします。これは、ここに当てはまります。そうである場合は、「"The number 6 is smaller than ten." 6は10より小さい」と出力されます。



`else`キーワードを使用して式が真でない場合に*のみ*特定のコードを実行し、`elseif`条件ステートメントをチェーン化することもできます。



```lua
local number = 15

if number < 10 then
	print("The number is smaller than ten.")
elseif number < 100 then
	print("The number is bigger than or equal to ten, but smaller than one hundred.")
elseif number ~= 1000 and number < 3000 then
	print("The number is bigger than or equal to one hundred, smaller than three thousands and is not exactly one thousand.")
else
	print("The number is either 1000 or bigger than 2999.")
end
```

`else`ブロックは常に最後のものでなければならないことに注意してください。`elseif`ブロックの後に`else`ブロックを置くことはできません。`elseif`ブロックは、それらを先行ブロックのいずれも実行されなかった場合にのみ意味があります。



2つの値を比較するために使用される演算子は、上記のコードで使用されているものもあり、関係演算子と呼ばれます。関係がtrueの場合、ブール値`true`を返します。それ以外の場合は、ブール値 `false` を返します。



|                 | 等しい | 等しくない | より大きい | 未満 | 以上 | 以下 |
| --------------- | ------ | ---------- | ---------- | ---- | ---- | ---- |
| 数学表記        | =      | ≠          | >          | <    | ≥    | ≤    |
| Luaオペレーター | ==     | 〜=        | >          | <    | >=   | <=   |

|                       | equal to | not equal to | greater than | less than | greater than or equal to | less than or equal to |
| --------------------- | -------- | ------------ | ------------ | --------- | ------------------------ | --------------------- |
| Mathematical notation | =        | ≠            | >            | <         | ≥                        | ≤                     |
| Lua operator          | ==       | ~=           | >            | <         | >=                       | <=                    |

上記のコードは、`and`キーワードを使用して、条件式で多くのブール式を組み合わせる方法も示しています。



## Loops

多くの場合、プログラマーは特定のコードまたは同様のコードを何度も実行するか、ユーザー入力に応じて特定のコードを何度も実行する必要があります。ループは、1回指定されますが、連続して複数回実行される可能性のある一連のステートメントです。



### Condition-controlled loops

条件制御ループは、条件によって制御されるループです。これらは条件ステートメントに非常に似ていますが、条件がtrueの場合にコードを実行し、それ以外の場合はスキップする代わりに、条件がtrueの間、または条件がfalseになるまでコードを実行し続けます。 Luaには、と条件制御ループの2つのステートメントがあります。`while`ループと　`repeat`　ループです。このようなループはコードを実行し、条件が真であるかどうかを確認します。 trueの場合、コードを再度実行し、条件がfalseになるまで繰り返します。条件がfalseの場合、コードの繰り返しを停止し、プログラムフローが続行されます。コードの各実行は、 iteration（反復）と呼ばれます。`while`と`repeat`ループの違いは、`repeat`ループはループの最後に条件をチェックすることです。`while`ループは、ループの開始時にそれをチェックします。これは、最初の反復でのみ違いがあります。コードが最初に実行されたときに条件がfalseであっても、`repeat`ループは常に少なくとも1回はコードを実行します。これは、条件が実際に true である場合にのみコードを最初に実行する`while`ループには当てはまりません。



```lua
local number = 0

while number < 10 do
	print(number)
	number = number + 1 -- Increase the value of the number by one.
end
```

上記のコードは、0、1、2、3のように、9まで出力します。10回目の反復後、数値は10以上になるため、ループの実行は停止します。ループは永久に実行されることを意味する場合があり、その場合、ループは無限ループと呼ばれます。たとえば、レンダラー、つまり画面上に物を描画するソフトウェアプロセスは、ユーザーに表示される画像を更新するために画面を再描画するために絶えずループすることがよくあります。これはビデオゲームでよくあることで、ユーザーに表示されるものを最新の状態に保つために、ゲームビューを常に更新する必要があります。ただし、ループを永久に実行する必要がある場合はまれであり、そのようなループはエラーの結果であることがよくあります。無限ループは多くのコンピュータリソースを消費する可能性がありますが、したがって、ユーザーから予期しない入力を受け取った場合でも、ループが常に終了するようにすることが重要です。



```lua
local number = 0

repeat
	print(number)
	number = number + 1
until number >= 10
```

上記のコードは、上記の`while`ループを使用したコードとまったく同じことを行います。主な違いは``while`キーワードと`do`キーワードの間に条件が配置される`while`ループとは異なり、条件はループの最後、untilキーワードの後に配置されることです。`repeat`ループは、`end`キーワードによってブロックが閉じられていないLuaで唯一のステートメントです。



### Count-controlled loops

変数をインクリメントすると、その値が段階的に、特に1ステップづつ増加します。前のセクションの2つのループは、変数の数字をインクリメントし、それを使用してコードを特定の回数実行しました。この種のループは非常に一般的であるため、Luaを含むほとんどの言語には組み込みのループ制御構造があります。この制御構造はカウント制御ループと呼ばれ、Luaおよびほとんどの言語では、`for`ステートメントによって定義されます。このようなループで使用される変数は、ループカウンターと呼ばれます。



```lua
for number = 0, 9, 1 do
	print(number)
end
```

上記のコードは、前のセクションで示した2つのループとまったく同じことを行いますが、数値変数はループのローカルであるため、ループ内からのみアクセスできます。変数名と等号記号に続く最初の数字は初期化です。ループカウンタが初期化される値です。 2番目の番号は、ループが停止する番号です。変数をインクリメントし、変数がこの数に達するまでコードを繰り返します。最後に、3番目の数値は増分です。これは、各反復でループカウンターが増加する値です。増分が指定されていない場合、Luaでは1と見なされます。したがって、以下のコードは1、1.1、1.2、1.3、1.4、1.5を出力します。



```lua
for n = 1, 2, 0.1 do
	print(n)
	if n >= 1.5 then
		break -- Terminate the loop instantly and do not repeat.
	end
end
```

上記のコードが2までではなく、1.5までしか上がらない理由は、ループを即座に終了する`break`ステートメントのためです。このステートメントは、`while`ループや`repeat`ループを含む任意のループで使用できます。ここでは`>=`演算子が使用されていることに注意してください。ただし、理論的には`==`演算子も同様に機能します。これは、10進数の精度エラーが原因です。Luaは、[倍精度浮動小数点形式で](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Double-precision_floating-point_format&usg=ALkJrhjTDYhvCEmzPxYqVGhWsVnOuke6CA)数値を表します、実際の値の近似値をメモリに格納します。場合によっては、近似の値が数値と正確に一致しますが、場合によっては、概算にすぎません。通常、これらの近似値は、違いが生じないように数値に十分に近いものになりますが、このシステムでは、等式演算子`==`を使用するとエラーが発生する可能性があります。これが、等式演算子の使用を避けて10進数で作業するのが一般的に安全である理由です。この特定のケースでは、等式演算子が使用されていた場合、コードは機能しませんでした[ [1\]](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version&usg=ALkJrhh-N6LiHOskM-AjeqBm6bGdgeh7sQ#cite_note-1)（1.9まで上昇し続けました）が、`>=` 演算子では機能します。



## Blocks

ブロックは、順番に実行されるステートメントのリストです。これらのステートメントには、命令を含まない空のステートメントを含めることができます。空のステートメントを使用して、セミコロンでブロックを開始したり、2つのセミコロンを順番に書き込んだりできます。



関数の呼び出しと割り当ては括弧で始まる場合があり、あいまいさを招く可能性があります。このフラグメントの例です：



```lua
a = b + c
(print or io.write)('done')
```

このコードは、次の2つの方法で解釈できます。



```lua
a = b + c(print or io.write)('done')
a = b + c; (print or io.write)('done')
```

現在のパーサーは、常に最初の方法でそのような構文を認識し、最初の括弧を呼び出しの引数の開始として解釈します。このあいまいさを回避するために、次のように常に括弧で始まるセミコロンステートメントを前に付けることをお勧めします。



```lua
;(print or io.write)('done')
```

### Chunks

Luaのコンパイル単位はチャンクと呼ばれます。チャンクは、ホストプログラム内のファイルまたは文字列に格納できます。チャンクを実行するために、Luaは最初にチャンクを仮想マシンの命令にプリコンパイルし、次にコンパイルされたコードを仮想マシンのインタープリターで実行します。チャンクは、Luaに付属のコンパイルプログラム`luac`、または指定された関数のバイナリ表現を含む文字列を返す`string.dump` 関数を使用して、バイナリ形式（バイトコード）にプリコンパイルすることもできます。



この`load`関数を使用して、チャンクをロードできます。`load`関数に指定された最初のパラメーターが文字列の場合、チャンクはその文字列です。この場合、文字列はLuaコードまたはLuaバイトコードのいずれかです。最初のパラメーターが関数の場合、`load`チャンクを取得するためにその関数を繰り返し呼び出します。各チャンクは、前の文字列と連結される文字列です。次に、何も返されないか、空の文字列が返されたときに、チャンクが完了したと見なされます。



`load`関数は構文エラーがない場合は関数としてコンパイルされたチャンクを返します。それ以外の場合は、`nil`とエラーメッセージが返されます。



`load`関数の2番目のパラメーターは、チャンクのソースを設定するために使用されます。すべてのチャンクは、適切なエラーメッセージとデバッグ情報を提供できるように、ソースのコピーをチャンク内に保持します。デフォルトでは、それらのソースのコピーは`load`に与えられたコードになります（コードが与えられた場合、代わりに関数が与えられた場合、それは「=(load)」になります）。このパラメーターを使用して変更できます。これは、元のソースを取り戻せないようにコードをコンパイルするときに最も役立ちます。次に、バイナリ表現に含まれているソースを削除する必要があります。そうしないと、元のコードを取得できるためです。



`load`関数の3番目のパラメーターは、生成された関数の環境を設定するために使用でき、4番目のパラメーターは、チャンクをテキストにするかバイナリにするかを制御します。文字列「b」（バイナリチャンクのみ）、「t」（テキストチャンクのみ）、または「bt」（バイナリとテキストの両方）の場合があります。デフォルトは「bt」です。



`load`とまったく同じように機能する` loadfile`関数もありますが、この関数はファイルからコードを取得するものです。 最初のパラメーターは、コードを取得するファイルの名前です。 バイナリ表現に格納されているソースを変更するパラメータはありません。`load`関数の3番目と4番目のパラメータは、この関数の2番目と3番目のパラメータに対応しています。 `loadfile`関数を使用して、標準入力からコードをロードすることもできます。これは、ファイル名が指定されていない場合に実行されます。



この`dofile`関数は`loadfile`関数に似ていますが、コードを関数としてファイルにロードする代わりに、ソースコードファイルに含まれているコードをLuaチャンクとしてすぐに実行します。その唯一のパラメーターは、コンテンツを実行するファイルの名前を指定するために使用されます。引数が指定されていない場合は、標準入力の内容が実行されます。チャンクが値を返す場合、それらは`dofile`関数の呼び出しによって提供されます。`dofile`はプロテクトモードでは実行されないため、`dofile`で実行されたチャンク内のすべてのエラーが伝播します。



1. [↑](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_ref-1) http://codepad.org/kYHPSvqx



# Functions

スタックとそのスタックで実行できる操作の図。

![An illustration of a stack and of the operations that can be performed on it.](https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Data_stack.svg/320px-Data_stack.svg.png)




スタックは、*後入れ先出しの*原則に従って動作する、アイテムを追加（*プッシュ*）または削除（*ポップ*）できるアイテムのリストです。つまり、最後に追加されたアイテムが最初に削除されます。このようなリストがスタックと呼ばれるのはこのためです。スタックでは、最初にその上にあるアイテムを削除せずにアイテムを削除することはできません。したがって、すべての操作はスタックの最上位（Top）で行われます。アイテムは、他のアイテムの後に追加された場合は上にあり、他のアイテムの前に追加された場合は下にあります。



関数（サブルーチン、プロシージャ、ルーチン、またはサブプログラムとも呼ばれます）は、特定のタスクを実行する一連の命令であり、その一連の命令を実行する必要があるときはいつでも、プログラムの他の場所から*呼び出す*ことができます。関数は、入力として値を受け取り、入力を操作したり、入力に基づいてタスクを実行したりした後、出力を返すこともできます。関数は、他の関数内を含め、プログラム内のどこからでも定義できます。また、関数にアクセスできるプログラムの任意の部分から呼び出すこともできます。関数は、数値や文字列と同様に値であるため、変数に格納できます。変数に共通するすべてのプロパティがあります。これらの特性により、関数はとてもつかいやすくなります。



関数は他の関数から呼び出すことができるため、Luaインタープリター（Luaコードを読み取って実行するプログラム）は、関数が終了したとき（それ以上実行するコードがないとき）に、現在実行している関数と呼ばれる関数を認識できる必要があります。それによって正しい関数の実行に戻ることができます。これは、コールスタックと呼ばれるスタックを使用して行われます。コールスタック内の各アイテムは、現在実行されている関数で、スタック内のすぐ上にあるアイテムがなくなるまで呼び出す関数です。関数が終了すると、インタープリターはスタックのポップ操作を使用してリスト内の最後の関数を削除し、その後、前の関数に戻ります。



関数には、組み込み関数とユーザー定義関数の2種類があります。組み込み関数はLuaで提供される関数であり、すでに知っている`print`関数などの関数が含まれています。print関数のように直接アクセスできるものもあれば、乱数を返す`math.random`関数のようにライブラリを介してアクセスする必要があるものもあります。ユーザー定義関数は、ユーザーが定義した関数です。ユーザー定義関数は、関数コンストラクターを使用して定義されます。



```lua
local func = function(first_parameter, second_parameter, third_parameter)
	-- function body (a function's body is the code it contains)
end
```

上記のコードは、3つのパラメーターを持つ関数を作成し、それを変数funcに格納します。次のコードは上記のコードとまったく同じですが、関数を定義するためにシンタックスシュガーを使用しています。



```lua
local function func(first_parameter, second_parameter, third_parameter)
	-- function body
end
```

なお、第2の形式を使用する場合は、内部から関数を参照することができますが、第1の形式を使用する場合は参照できません。これは、`local function foo() end`が `local foo = function() end`ではなく`local foo; foo = function() end`に変換されるためです。これは、fooが1番目の形式ではなく2番目の形式の関数の環境の一部であることを意味します。これは、なぜ2番目の形式が関数自体を参照できるかを説明しています。



どちらの場合も、`local`キーワードを省略して関数をグローバル変数に格納することができます。パラメータは変数のように機能し、関数が値を受け取ることを可能にします。関数が呼び出されると、引数が与えられます。その後、関数はそれらをパラメーターとして受け取ります。パラメータは、関数の先頭で定義されたローカル変数のようなものであり、関数呼び出しで指定された引数の順序に応じて順番に割り当てられます。引数が欠落している場合、パラメーターの値は`nil`になります。次の例の関数は、2つの数値を加算し、結果を出力します。したがって、コードの実行時に5が出力されます。



```lua
local function add(first_number, second_number)
	print(first_number + second_number)
end

add(2, 3)
```

関数呼び出しは、ほとんどの場合、フォーム`name(arguments)`の下にあります。ただし、引数が1つだけで、それがテーブルまたは文字列であり、変数に含まれていない場合（つまり、関数呼び出しで直接作成され、リテラルとして表される場合）、括弧は省略できます。



```lua
print "Hello, world!"
print {4, 5}
```

前の例のコードの2行目は、テーブルのメモリアドレスを出力します。`print`関数が自動的に値を文字列に変換すると、複合型（関数、テーブル、ユーザーデータ、スレッド）がそれらのメモリアドレスに変更されます。ただし、ブール値、数値、および nil 値は、対応する文字列に変換されます。

The second line of code in the previous example would print the memory address of the table. When converting values to strings, which the `print` function does automatically, complex types (functions, tables, userdata and threads) are changed to their memory addresses. Booleans, numbers and the nil value, however, will be converted to corresponding strings.

*パラメータ*と*引数*という用語は、同じ意味で使われることがよくあります。この本では、適切な意味で、*パラメータ*と*引数*という用語は、それぞれ、パラメータとして割り当てられて関数に渡される値と対応する引数として値が割り当てられるものの名前を意味します。

The terms *parameter* and *argument* are often used interchangeably in practice. In this book, and in their proper meanings, the terms *parameter* and *argument* mean, respectively, a name to which the value of the corresponding argument will be assigned and a value that is passed to a function to be assigned to a parameter.

## Returning values

関数は入力を受け取り、それを操作し、出力を返すことができます。入力（パラメーター）を受け取り、それを操作する方法（関数本体）は既に知っています。また、returnステートメントを使用して、任意のタイプの1つまたは複数の値を返すことによって出力することもできます。これが、関数呼び出しがステートメントと式の両方である理由です。それらは実行できますが、評価することもできます。

Functions can receive input, manipulate it and give back output. You already know how they can receive input (parameters) and manipulate it (function body). They can also give output by returning one or many values of any type, which is done using the return statement. This is why function calls are both statements and expressions: they can be executed, but they can also be evaluated.

```lua
local function add(first_number, second_number)
	return first_number + second_number
end

print(add(5, 6))
```

上記の関数のコードは、最初に`add`関数を定義しています。次に、5と6を値として呼び出します。`add`関数はそれらを加算して結果を返し、出力されます。これが、上記のコードが11を出力する理由です。これらの値に評価される式をコンマで区切ることにより、関数が多くの値を返すことも可能です。

The code in the above function will first define the function `add`. Then, it will call it with 5 and 6 as values. The function will add them and return the result, which will then be printed. This is why the code above would print 11. It is also possible for a function to return many values by separating the expressions that evaluate to these values with commas.

## Errors

エラーには、構文エラー、静的セマンティックエラー、セマンティックエラーの3種類があります。構文エラーは、コードが明らかに無効な場合に発生します。たとえば、次のコードはLuaによって無効として検出されます。

There are three types of errors: syntactic errors, static semantic errors and semantic errors. Syntactic errors happen when code is plainly invalid. The following code, for example, would be detected by Lua as invalid:

```lua
print(5 ++ 4 return)
```
上記のコードは意味がありません。それから意味を引き出すことは不可能です。同様に、英語では、「cat（猫）　dog（犬）　tree（木）」は意味がないため、構文的に有効ではありません。文を作成するための規則に従っていません。

The code above doesn't make sense; it is impossible to get a meaning out of it. Similarly, in English, "cat dog tree" is not syntactically valid because it has no meaning. It doesn't follow the rules for creating a sentence.

静的セマンティックエラーが起こるのはコードは意味を持っているが、まだ成立しない場合です。例えば、文字列に対して数字を足そうとすると静的セマンティックエラーになります。
これは文字列に数字を加算できないためです。

Static semantic errors happen when code has a meaning, but still doesn't make sense. For example, if you try adding a string with a number, you get a static semantic error because it is impossible to add a string with a number:

```lua
print("hello" + 5)
```

上記のコードはLuaの構文規則には従いますが、数値を含む文字列を追加することは不可能であるため、意味が成立しません（文字列が数値を表す場合を除き、その場合は強制的に1つになります）。これは英語で「I are big」という文と比較することができます。英語で文章を作成するための規則に収まっていますが、「I」は単数形で「are」は複数形であるため、それでもやはりおかしいわけです。

The code above follows Lua's syntactic rules, but it still doesn't make sense because it is impossible to add a string with a number (except when the string represents a number, in which case it will be coerced into one). This can be compared in English to the sentence "I are big". It follows the rules for creating sentences in English, but it still doesn't make sense because "I" is singular and "are" is plural.

最後に、セマンティックエラーは、コードの一部の意味がその作成者が考えているものではない場合に発生するエラーです。これらは見つけるのが非常に難しいため、最悪のエラーです。 Luaは、構文エラーまたは静的セマンティックエラー（これはエラーのスローと呼ばれます）がある場合は常に通知しますが、セマンティックエラーがある場合は、どのような考えでコードが意味づけされていたかわからないため、通知できません。これらのエラーは、思っているよりも頻繁に発生し、エラーを見つけて修正することに、多くのプログラマーがたくさんの時間を費やしています。

Finally, semantic errors are errors that happen when the meaning of a piece of code is not what its creator thinks it is. Those are the worst errors because they can be very hard to find. Lua will always tell you when there is a syntactic error or a static semantic error (this is called throwing an error), but it cannot tell you when there is a semantic error since it doesn't know what you think the meaning of the code is. These errors happen more often than most people would think they do and finding and correcting them is something many programmers spend a lot of time doing.

エラーを見つけて修正するプロセスは、デバッグと呼ばれます。ほとんどの場合、プログラマーは実際にエラーを修正するよりもエラーを見つけることに多くの時間を費やします。これは、すべてのタイプのエラーに当てはまります。問題が何であるかがわかれば、通常は簡単に修正できますが、プログラマーがコードのどこに問題があるのかを見つけられずに、何時間もコードを見直す場合もあります。

The process of finding errors and correcting them is called debugging. Most of the time, programmers will spend more time finding errors than actually correcting them. This is true for all types of errors. Once you know what the problem is, it is usually simple to fix it, but sometimes, a programmer can look at a piece of code for hours without finding what is wrong in it.

### Protected calls

エラーをスローすることは、インタープリター（コードを読み取って実行するプログラム）によって手動で行われたか自動で行われたかにかかわらず、コードに問題があることを示すアクションです。指定されたコードが無効な場合、Luaによって自動的に実行されますが、`error`関数を使用して手動で実行できます。

Throwing an error is the action of indicating, whether it is done manually or automatically by the interpreter (the program that reads the code and executes it), that something is wrong with the code. It is done automatically by Lua when the code given is invalid, but it can be done manually with the `error` function:

```lua
local variable = 500
if variable % 5 ~= 0 then
	error("It must be possible to divide the value of the variable by 5 without obtaining a decimal number.")
end
```

`error`関数には、エラーがスローされるスタックレベルを示す2番目の引数もありますが、これについては本書では取り上げません。この`assert`関数は`error`関数と同じことを行いますが、最初の引数が nil または false と評価され、エラーをスローするスタックレベルを指定するために使用できる引数がない場合にのみエラーをスローします。` assert`関数は、スクリプトの開始時に役立ちます。たとえば、スクリプトが機能するために必要なライブラリが使用可能かどうかを確認する場合などです

The `error` function also has a second argument, which indicates the stack level at which the error should be thrown, but this will not be covered in this book. The `assert` function does the same thing as the `error` function, but it will only throw an error if its first argument evaluates to nil or false and it doesn't have an argument that can be used to specify the stack level at which the error should be thrown. The assert function is useful at the start of a script, for example, to check if a library that is required for the script to work is available.

エラーがスローされるたびにプログラム内のコードの実行が停止するため、なぜ自発的にエラーをスローしたいのか理解するのは難しいかもしれませんが、多くの場合、関数が正しく使用されていないときやプログラムが適切な環境で実行されていないときにエラーをスローし、コードをデバッグしなければならない人が、何が悪いのか気付かずにコードを長時間見つめることなく、速く間違いを見つけるのに役立ちます。

It may be hard to understand why one would desire to voluntarily throw an error, since the code in a program stops running whenever an error is thrown, but, often, throwing errors when functions are used incorrectly or when a program is not running in the right environment can be helpful to help the person who will have to debug the code to find it immediately without having to stare at the code for a long time without realizing what is wrong.

エラーがコードを停止するのを防ぎ、代わりにユーザーにエラーメッセージを表示して、開発者にバグを報告できるようにすることが役立つ場合があります。これは例外処理（またはエラー処理）と呼ばれ、エラーをキャッチして伝播を防ぎ、例外ハンドラーを実行して処理することで実行されます。さまざまなプログラミング言語でこの方法は大きく異なります。Luaでは、プロテクトされた呼び出しを使用して行われます[[1\]](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_note-2)。プロテクトモードで呼び出された関数は、エラーが発生してもプログラムを停止しないため、これらはプロテクト呼び出しと呼ばれます。プロテクトモードで関数を呼び出すために使用できる関数は2つあります。

Sometimes, it can be useful to prevent an error from stopping the code and instead do something like displaying an error message to the user so he can report the bug to the developer. This is called exception handling (or error handling) and is done by catching the error to prevent its propagation and running an exception handler to handle it. The way it is done in different programming languages varies a lot. In Lua, it is done using protected calls[[1\]](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_note-2). They are called protected calls because a function called in protected mode will not stop the program if an error happens. There are two functions that can be used to call a function in protected mode:

| 関数                             | 説明                                                         |
| -------------------------------- | ------------------------------------------------------------ |
| `pcall(function, ...)`           | プロテクトモードで関数を呼び出し、ステータスコード（エラーがスローされたかどうかによって値が異なるブール値）と関数によって返される値、または関数がエラーによって停止された場合はエラーメッセージを返します。引数は、プロテクトモードで呼び出す必要のある関数である最初の引数の後に`pcall`関数に渡すことで関数に指定できます。 |
| `xpcall(function, handler, ...)` | pcallと同じことを行いますが、関数エラーが発生すると、pcallが返すのと同じ値を返す代わりに、それらをパラメーターとしてハンドラー関数を呼び出します。次に、ハンドラ関数を使用して、たとえば、エラーメッセージを表示できます。`pcall`関数に関しては、`xpcall`関数に対して引数として与えることで関数に引数を渡すことができます。 |

| Function                         | Description                                                  |
| -------------------------------- | ------------------------------------------------------------ |
| `pcall(function, ...)`           | Calls the function in protected mode and returns a status code (a boolean value whose value depends on if an error was thrown or not) and the values returned by the function, or the error message if the function was stopped by an error. Arguments can be given to the function by passing them to the `pcall` function after the first argument, which is the function that should be called in protected mode. |
| `xpcall(function, handler, ...)` | Does the same thing as pcall, but, when the function errors, instead of returning the same values as those pcall would return, it calls the handler function with them as parameters. The handler function can then be used, for example, to display an error message. As for the `pcall` function, arguments can be passed to the function by being given to the `xpcall` function. |

## Stack overflow

呼び出しスタック、つまり呼び出された順序で呼び出されたすべての関数を含むスタックについては、前述しました。Luaを含むほとんどの言語でのその呼び出しスタックには、最大サイズがあります。この最大サイズは非常に大きいため、ほとんどの場合心配する必要はありませんが、自分自身を呼び出す関数（これは再帰性と呼ばれ、このような関数は再帰関数と呼ばれます）は、自分自身を呼び出すことを妨げるものがない場合、この制限に達するまで無期限に再帰を続ける可能性があります。これはスタックオーバーフローと呼ばれます。スタックがオーバーフローすると、コードの実行が停止し、エラーがスローされます。

The call stack, the stack that contains all the functions that were called in the order in which they were called, was mentioned earlier. That call stack in most languages, including Lua, has a maximum size. This maximum size is so big that it should not be worried about in most cases, but functions that call themselves (this is called recursivity and such functions are called recursive functions) can reach this limit if there is nothing to prevent them from calling themselves over and over indefinitely. This is called a stack overflow. When the stack overflows, the code stops running and an error is thrown.

## Variadic functions

可変引数関数は、vararg関数とも呼ばれ、可変数の引数を受け入れる関数です。可変個引数関数は、パラメーターリストの最後にある3つのドット（ "..."）で示されます。パラメータリストのパラメータに収まらない引数は、破棄されるのではなく、vararg式を介して関数で使用できるようになります。これも3つのドットで示されます。 vararg式の値は、値のリスト（テーブルではない）であり、次の式を使用して、より簡単に操作できるようにテーブルに配置できます。

`{...}`

Lua 5.0では、vararg式を介して使用できる代わりに、「arg」という特別なパラメーターで追加の引数を使用できました。次の関数は、受け取ったすべての引数に最初の引数を追加し、次にそれらすべてを合計して結果を出力する関数の例です。

Variadic functions, which are also called vararg functions, are functions that accept a variable number of arguments. A variadic function is indicated by three dots ("...") at the end of its parameter list. Arguments that do not fit in the parameters in the parameter list, instead of being discarded, are then made available to the function through a vararg expression, which is also indicated by three dots. The value of a vararg expression is a list of values (not a table) which can then be put in a table to be manipulated with more ease with the following expression: `{...}`. In Lua 5.0, instead of being available through a vararg expression, the extra arguments were available in a special parameter called "arg". The following function is an example of a function that would add the first argument to all the arguments it receives, then add all of them together and print the result:

```lua
function add_one(increment, ...)
	local result = 0
	for _, number in next, {...} do
		result = result + number + increment
	end
end
```

上記のコードは可変個引数関数のデモンストレーションにすぎないため、理解する必要はありません。

It is not necessary to understand the code above as it is only a demonstration of a variadic function.

この`select`関数は、テーブルを使用せずに引数リストを操作するのに役立ちます。引数の数が不定であるため、それ自体がvariadic関数です。最初の引数として指定された番号を使用して、引数の後のすべての引数を返します（指定された番号が負の場合、最後からインデックスを付けます。つまり、-1が最後の引数です）。また、最初の引数が文字列 "＃"の場合、最初の引数を除いて、受け取った引数の数も返します。引数リスト内の特定の数より前のすべての引数を破棄すると、より元々は、引数として送信されるnil値と、引数として送信されない値を区別するのに役立ちます。`#`は最初の引数として、値が無いことから nil 値が指定されると`select`は区別します。引数リスト（および戻りリストも）はタプル（tuples:いくつかの部分からなるデータの構造）のインスタンスであり、テーブルに関する章で説明します。この`select`関数はすべてのタプルで機能します。

The `select` function is useful to manipulate argument lists without needing to use tables. It is itself a variadic function, as it accepts an indefinite number of arguments. It returns all arguments after the argument with the number given as its first argument (if the number given is negative, it indexes starting from the end, meaning -1 is the last argument). It will also return the number of arguments it received, excluding the first one, if the first argument is the string "#". It can be useful to discard all arguments in an argument list before a certain number, and, more originally, to distinguish between nil values being sent as arguments and nothing being sent as an argument. Indeed, `select` will distinguish, when `"#"` is given as its first argument, nil values from no value. Argument lists (and return lists as well) are instances of tuples, which will be explored in the chapter about tables; the `select` function works with all tuples.

```lua
print((function(...) return select('#', ...) == 1 and "nil" or "no value" end)()) --> no value
print((function(...) return select('#', ...) == 1 and "nil" or "no value" end)(nil)) --> nil
print((function(...) return select('#', ...) == 1 and "nil" or "no value" end)(variable_that_is_not_defined)) --> nil

-- As this code shows, the function is able to detect whether the value nil was passed as an argument or whether there was simply no value passed.
-- In normal circumstances, both are considered as nil, and this is the only way to distinguish them.
```

1. [↑](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version&usg=ALkJrhh-N6LiHOskM-AjeqBm6bGdgeh7sQ#cite_ref-2)詳細については、Ierusalimschy、Roberto（2003）を参照してください。 ["Error Handling in Application Code"](http://www.lua.org/pil/24.3.1.html). [*Programming in Lua*](http://www.lua.org/pil/contents.html) (first ed.). Lua.org. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [8590379817](https://en.m.wikibooks.org/wiki/Special:BookSources/8590379817). http://www.lua.org/pil/24.3.1.html. Retrieved June 20, 2014.
2. [↑](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_ref-2) For more information, see: Ierusalimschy, Roberto (2003). ["Error Handling in Application Code"](http://www.lua.org/pil/24.3.1.html). [*Programming in Lua*](http://www.lua.org/pil/contents.html) (first ed.). Lua.org. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [8590379817](https://en.m.wikibooks.org/wiki/Special:BookSources/8590379817). http://www.lua.org/pil/24.3.1.html. Retrieved June 20, 2014.

# Standard libraries

Luaは「バッテリーが付属していない」と言われている言語です。これは、そのライブラリがいくつかのことを行うために必要な最小限に保たれていることを意味します。Luaはコミュニティに依存して、より具体的なタスクを実行するために使用できるライブラリを作成しています。Luaには10のライブラリがあります。*Luaのリファレンスマニュアルは、*すべてのライブラリのドキュメントを提供しています[[1\]](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version&usg=ALkJrhh-N6LiHOskM-AjeqBm6bGdgeh7sQ#cite_note-3)。ここで簡単に説明されています[[2\]](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version&usg=ALkJrhh-N6LiHOskM-AjeqBm6bGdgeh7sQ#cite_note-4)。基本ライブラリとパッケージライブラリを除くすべてのライブラリは、テーブルのフィールドとして関数と値を提供します。

Lua is a language that is said to "not be provided with batteries". This means that its libraries are kept to the minimum necessary to do some stuff. Lua relies on its community to create libraries that can be used to perform more specific tasks. There are ten libraries available in Lua. The *Lua Reference Manual* provides documentation for all the libraries[[1\]](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_note-3), so they will only be briefly described here[[2\]](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_note-4). All the libraries except the basic and the package libraries provide their functions and values as fields of a table.

## Basic library

基本ライブラリはLuaにコア機能を提供します。そのすべての関数と値はグローバル環境で直接利用可能であり、デフォルトでグローバル環境で直接利用可能なすべての関数と値は基本ライブラリの一部です。

The basic library provides core functionality to Lua. All its functions and values are directly available in the global environment, and all functions and values available directly in the global environment by default are part of the basic library.

### Assertion

アサーションは、開発者が true であると想定する述語です。これらは、プログラムの実行の特定の瞬間に特定の条件が真であることを保証するためにプログラムで使用されます。アサーションは、プログラムが正しく機能することを確認するための[unit tests](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.m.wikibooks.org/w/index.php%3Ftitle%3DLua_Programming/Unit_testing%26action%3Dedit%26redlink%3D1&usg=ALkJrhgO49Wfq8PkkhqVgyO8fwPyXEAHxA)で使用されますが、プログラムコードでも使用されます。この場合、アサーションが false の場合、プログラムが正しい環境を確認するため、またはプログラムコードでエラーが発生していないことを確認し、適切なエラーメッセージを生成して、予期したとおりに何かが発生しなかったときにコードのバグを見つけやすくします。 Luaでは、条件とメッセージ（デフォルトでは「アサーションに失敗しました！」）をパラメーターとして受け入れる`assert`関数を使用してアサーションが作成されます。条件が false と評価された場合、`assert`はメッセージとともにエラーをスローします。true と評価された場合は、`assert`はすべての引数を返します。

An assertion is a predicate that is assumed by the developer to be true. They are used in programs to ensure that a specific condition is true at a specific moment of the execution of a program. Assertions are used in [unit tests](https://en.m.wikibooks.org/w/index.php?title=Lua_Programming/Unit_testing&action=edit&redlink=1) to verify that a program works correctly, but are also used in program code, in which case the program will fail when an assertion is false, either to verify that the environment in which the program is correct, or to verify that no error was made in program code and to generate appropriate error messages to make it easier to find bugs in the code when something doesn't happen as expected. In Lua, assertions are made with the `assert` function, which accepts a condition and a message (which will default to "assertion failed!") as parameters. When the condition evaluates to false, `assert` throws an error with the message. When it evaluates to true, `assert` returns all its arguments.

### Garbage collection

ガベージコレクションは、Luaや他の多くの言語で実装されている自動メモリ管理の一形態です。プログラムがデータを変数に格納する必要がある場合、プログラムはオペレーティングシステムに、変数の値を格納するためにコンピュータのメモリにスペースを割り当てるように要求します。次に、スペースが不要になると（通常、変数がスコープから外れたため）、別のプログラムがスペースを使用できるように、スペースの割り当てを解除するようにオペレーティングシステムに指示します。 Luaでは、実際のプロセスははるかに複雑ですが、基本的な考え方は同じです。プログラムは、変数の値が不要になったときにオペレーティングシステムに通知する必要があります。低水準言語では、割り当ては言語によって処理されますが、割り当て解除は、プログラマーが値を必要としなくなったときに言語が認識できないためではありません。値を参照する変数がスコープから外れたり削除されたりした場合でも、スクリプト内の別の変数またはフィールドがそれを参照している可能性があり、割り当てを解除すると問題が発生します。高水準言語では、割り当て解除は、Luaが使用するシステムであるガベージコレクションなど、さまざまな自動メモリ管理システムによって処理される場合があります。ガベージコレクターは、Luaによって割り当てられたすべての値を定期的に検索して、どこにも参照されていない値を探します。プログラムがアクセスできなくなった値を収集し（参照がないため）、これらの値を安全に割り当て解除できることがわかっているため、割り当てを解除します。これはすべて透過的かつ自動的に行われるため、プログラマーは通常、それについて何もする必要はありません。しかし、時々、開発者は、ガベージコレクターに指示を与えることができます。

Garbage collection is a form of automatic memory management implemented by Lua and many other languages. When a program needs to store data in a variable, it asks the operating system to allocate space in the computer's memory to store the variable's value. Then, when it doesn't need the space anymore (generally because the variable fell out of scope), it tells the operating system to deallocate the space so that another program may use it. In Lua, the actual process is much more complex, but the basic idea is the same: the program must tell the operating system when it doesn't need a variable's value anymore. In low level languages, allocation is handled by the language, but deallocation is not because the language cannot know when a programmer doesn't need a value anymore: even if a variable that referenced the value fell out of scope or was removed, another variable or a field in a script may still reference it, and deallocating it would cause problems. In higher level languages, deallocation may be handled by various automatic memory management systems, such as garbage collection, which is the system used by Lua. The garbage collector regularly searches through all the values allocated by Lua for values that are not referenced anywhere. It will collect values that the program cannot access anymore (because there is no reference to them) and, since it knows that these values can safely be deallocated, will deallocate them. This is all done transparently and automatically, so the programmer does not generally need to do anything about it. However, sometimes, the developer may want to give instructions to the garbage collector.

#### Weak references

弱参照は、[ガベージコレクターによって無視される参照](https://ja.wikipedia.org/wiki/%E5%BC%B1%E3%81%84%E5%8F%82%E7%85%A7)です。これらの参照は、開発者が `mode` メタメソッドを使用してガベージコレクターに示します。テーブルの `mode` メタメソッドは文字列である必要があります。その文字列に文字「k」が含まれている場合、テーブルのフィールドのすべてのキーは弱く、文字「v」が含まれている場合、テーブルのフィールドのすべての値は弱くなります。オブジェクトの配列に弱い値がある場合、ガベージコレクターは、その配列および他の弱い参照でのみ参照されている限り、その配列で参照されている場合でもこれらのオブジェクトを収集します。この動作は便利な場合もありますが、ほとんど使用されません。

Weak references are references that are ignored by the garbage collector. These references are indicated to the garbage collector by the developer, using the `mode` metamethod. A table's `mode` metamethod should be a string. If that string contains the letter "k", all the keys of the table's fields are weak, and if it contains the letter "v", all the values of the table's fields are weak. When an array of objects has weak values, the garbage collector will collect these objects even if they are referenced in that array, as long as they are only referenced in that array and in other weak references. This behavior is sometimes useful, but rarely used.

#### Manipulating the garbage collector

ガベージコレクターは、基本ライブラリの一部であり、ガベージコレクターへのインターフェイスとして機能する `collectgarbage` 関数で操作できます。その最初の引数は、実行するアクションをガベージコレクターに示す文字列です。2番目の引数は、一部のアクションで使用されます。この `collectgarbage` 関数を使用して、ガベージコレクターを停止し、手動で収集サイクルを実行し、Luaが使用するメモリをカウントできます。

The garbage collector may be manipulated with the `collectgarbage` function, which is part of the basic library and serves as an interface to the garbage collector. Its first argument is a string that indicates to the garbage collector what action should be performed; a second argument is used by some actions. The `collectgarbage` function can be used to stop the garbage collector, manually perform collection cycles and count the memory used by Lua.

## Coroutines

> **Coroutines**は、[サブルーチン](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/subroutine&usg=ALkJrhi8jzOULEjJ1hplRlFcGlV8gZcr1A)を一般化して、特定の場所で実行を一時停止および再開するための複数の[エントリポイント](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/entry_point&usg=ALkJrhixPlb6PyQYLsRnHACHiivW2ePROw)を許可する[コンピュータプログラム](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/computer_program&usg=ALkJrhgAvIURsjyE4JqxxgW2ym075csorQ)コンポーネントです。コルーチンは、[協調タスク](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/cooperative_multitasking&usg=ALkJrhiADjyfevkjw_WwIRcUOxersI1rFA)、[例外](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/exception_handling&usg=ALkJrhi6Dwz-mOPvvY0gX_crK2yqVehZdA)、[イベントループ](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/event_loop&usg=ALkJrhgZFK2afaQnYMYTsZQW6SeTfM648Q)、[イテレータ](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/iterator&usg=ALkJrhhlgP0_0SmgvvmITMRLx_wRnlww7g)、[無限リスト](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/lazy_evaluation&usg=ALkJrhi6cLQdDRdvh_DK9IAsxXK-vF8I7g)、[パイプ](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/pipeline_(software)&usg=ALkJrhhdyPCiI1O0UXvWU1Q1dAkZUaEmTg)など、より使い慣れたプログラムコンポーネントの実装に最適です。
>
> —ウィキペディア、[コルーチン](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/Coroutine&usg=ALkJrhjwxw7xoPpU8qfJJvK6w4Mnbf0rvw)

> **Coroutines** are [computer program](https://en.wikipedia.org/wiki/computer_program) components that generalize [subroutines](https://en.wikipedia.org/wiki/subroutine) to allow multiple [entry points](https://en.wikipedia.org/wiki/entry_point) for suspending and resuming execution at certain locations. Coroutines are well-suited for implementing more familiar program components such as [cooperative tasks](https://en.wikipedia.org/wiki/cooperative_multitasking), [exceptions](https://en.wikipedia.org/wiki/exception_handling), [event loop](https://en.wikipedia.org/wiki/event_loop), [iterators](https://en.wikipedia.org/wiki/iterator), [infinite lists](https://en.wikipedia.org/wiki/lazy_evaluation) and [pipes](https://en.wikipedia.org/wiki/pipeline_(software)).
>
> —Wikipedia, [Coroutine](https://en.wikipedia.org/wiki/Coroutine)

コルーチンは、Luaのコルーチンライブラリを使用して作成および操作できるコンポーネントであり、コルーチンを内部から生成する関数またはコルーチンを外部から再開する関数を呼び出すことにより、特定の場所で関数の実行を生成および再開できるようにします 。例：

Coroutines are components that can be created and manipulated with the coroutine library in Lua and that allow the yielding and resuming of the execution of a function at specific locations by calling functions that yield the coroutine from inside of itself or that resume it from outside of itself. Example:

1. メインスレッドの関数は、`coroutine.create`関数からコルーチンを作成し、`coroutine.resume`で再開します。コルーチンには、番号3が渡されます。
2. コルーチンの関数が実行され、引数として `coroutine.resume` に渡された数値を取得します。
3. 関数は、実行の特定の時点に到達し`coroutine.yield`、引数として、受け取った引数の合計（3）と2（したがって、3 + 2 = 5）を呼び出します。
4. `coroutine.resume`への呼び出しは` coroutine.yield`に渡されたため、5を返し、メインスレッドは現在再び実行されており、その数値を変数に格納します。 コードを実行した後、コルーチンを再開し、 `coroutine.resume`の呼び出しから受け取った値の2倍を` coroutine.resume`に渡します（つまり、5×2 = 10を渡します）。
5. コルーチンは、 `coroutine.yield` の呼び出しの結果として、`coroutine.resume` に渡された値を取得し、さらにコードを実行した後に終了します。 これは、 `coroutine.yield` の呼び出しの結果と、最初にパラメーターとして指定された値（つまり、10-3 = 7）との差を返します。
6. メインスレッドは、 `coroutine.resume` の呼び出しの結果としてコルーチンによって返される値を取得し、続行します。

1. A function in the main thread creates a coroutine from a function with `coroutine.create` and resumes it with `coroutine.resume`, to which the number 3 is passed.
2. The function in the coroutine executes and gets the number passed to `coroutine.resume` as an argument.
3. The function arrives at a certain point in its execution where it calls `coroutine.yield` with, as an argument, the sum of the argument it received (3) and 2 (hence, 3+2=5).
4. The call to `coroutine.resume` returns 5, because it was passed to `coroutine.yield`, and the main thread, now running again, stores that number in a variable. It resumes the coroutine again after having executed some code, passing to `coroutine.resume` the double of the value it has received from the call to `coroutine.resume` (i.e. it passes 5×2=10).
5. The coroutine gets the value passed to `coroutine.resume` as the result of the call to `coroutine.yield` and terminates after running some more code. It returns the difference between the result of the call to `coroutine.yield` and the value it was given as a parameter initially (i.e. 10−3=7).
6. The main thread gets the value returned by the coroutine as the result of the call to `coroutine.resume` and goes on.

この例をコードに入れると、次のようになります。

This example, put in code, gives the following:

```lua
local co = coroutine.create(function(initial_value)
	local value_obtained = coroutine.yield(initial_value + 2) -- 3+2=5
	return value_obtained - initial_value -- 10-3=7
end)

local _, initial_result = coroutine.resume(co, 3) -- initial_result: 5
local _, final_result = coroutine.resume(co, initial_result * 2) -- 5*2=10
print(final_result) --> 7
```

`coroutine.create`関数は、関数からコルーチンを作成します。 コルーチンは「スレッド」タイプの値です。 `coroutine.resume`は、コルーチンの実行を開始または継続します。 コルーチンは、エラーが発生した場合、または実行するものが何も残っていない場合（この場合、実行が終了した場合）にデッドと呼ばれます。 コルーチンがデッドの場合、再開することはできません。 `coroutine.resume`関数は、コルーチンの実行が成功した場合は` true`を返し、コルーチンが終了した場合は返されたすべての値とともに、終了しなかった場合は `coroutine.yield`に渡されます。 実行が成功しなかった場合は、エラーメッセージとともに「false」が返されます。 `coroutine.resume`は実行中のコルーチンを返し、そのコルーチンがメインスレッドの場合は` true`を返し、それ以外の場合は `false`を返します。

The `coroutine.create` function creates a coroutine from a function; coroutines are values of type "thread". `coroutine.resume` starts or continues the execution of a coroutine. A coroutine is said to be dead when it has encountered an error or has nothing left to run (in which case it has terminated its execution). When a coroutine is dead, it cannot be resumed. The `coroutine.resume` function will return `true` if the execution of the coroutine was successful, along with all the values returned, if the coroutine has terminated, or passed to `coroutine.yield` if it has not. If the execution was not successful, it will return `false` along with an error message. `coroutine.resume` returns the running coroutine and `true` when that coroutine is the main thread, or `false` otherwise.

この`coroutine.status`関数は、コルーチンのステータスを文字列として返します。

The `coroutine.status` function returns the status of a coroutine as a string:

* コルーチンが実行中の場合は「実行中」。つまり、 `coroutine.status`を呼び出したコルーチンである必要があります。
* コルーチンがyieldの呼び出しで一時停止されている場合、またはコルーチンがまだ実行を開始していない場合は、「一時停止」
* コルーチンがアクティブであるが実行されていない場合は「正常」、つまり別のコルーチンを再開したことを意味します
* コルーチンの実行が終了した場合、またはエラーが発生した場合は「デッド」

- "running" if the coroutine is running, which means it must be the coroutine which called `coroutine.status`
- "suspended" if the coroutine is suspended in a call to yield or if it has not started running yet
- "normal" if the coroutine is active but not running, which means it has resumed another coroutine
- "dead" if the coroutine has finished running or has encountered an error

`coroutine.wrap`関数は、呼び出されるたびにコルーチンを再開する関数を返します。 この関数に指定された追加の引数は、 `coroutine.resume`への追加の引数として機能し、コルーチンによって返される値、または` coroutine.yield`に渡される値は、関数の呼び出しによって返されます。 `coroutine.wrap`関数は、` coroutine.resume`とは異なり、プロテクトモードでコルーチンを呼び出さず、エラーを伝播します。

コルーチンには多くのユースケースがありますが、それらを説明することはこの本の範囲外です。

The `coroutine.wrap` function returns a function that resumes a coroutine every time it is called. Extra arguments given to this function will act as extra arguments to `coroutine.resume` and values returned by the coroutine or passed to `coroutine.yield` will be returned by a call to the function. The `coroutine.wrap` function, unlike `coroutine.resume`, does not call the coroutine in protected mode and propagates errors.

There are many use cases for coroutines, but describing them are outside the scope of this book.

## String matching

文字列を操作する場合、特定のパターンに従う部分文字列を文字列で検索できると便利なことがよくあります。 Luaには、これを行うための関数と、関数が文字列で検索できるパターンを表現するための表記法を提供する文字列操作ライブラリがあります。 Luaが提供する表記法は、プログラミングの世界のほとんどの言語やツールで使用されるパターンを表現するための[正規表現](https://translate.googleusercontent.com/translate_c?depth=1&pto=aue&rurl=translate.google.com&sl=en&sp=nmt4&tl=ja&u=https://en.wikipedia.org/wiki/regular_expression&usg=ALkJrhj_CdR0B83q433wqmYbGdMv6wD_lg)と非常によく似ています。ただし、それはより制限されており、構文がわずかに異なります。

When manipulating strings, it is frequently useful to be able to search strings for substrings that follow a certain pattern. Lua has a string manipulation library that offers functions for doing this and a notation for expressing patterns that the functions can search for in strings. The notation offered by Lua is very similar to [regular expressions](https://en.wikipedia.org/wiki/regular_expression), a notation for expressing patterns used by most languages and tools in the programming world. However, it is more limited and has slightly different syntax.

文字列ライブラリの`find`関数は、文字列内のパターンの最初の一致を探します。文字列内でパターンが見つかった場合、そのパターンが開始および終了する文字列内のインデックス（最初の文字から始まる文字列内の文字の位置を表す整数）を返します。パターンの出現が見つからない場合は、何も返しません。受け入れる最初のパラメーターは文字列で、2番目はパターン、3番目は`find`関数が検索を開始する文字位置を示す整数です。最後に、4番目の引数として`true`値を指定することにより、パターンなしで単純な一致を実行するように`find`関数に指示できます。次に、最初の文字列で指定された2番目の文字列の出現を検索します。単純一致を実行する場合は、3番目の引数を指定する必要があります。このサンプルコードは、文中の「lazy」という単語を検索し、その単語で見つかった出現箇所の開始位置と終了位置を出力します。

The `find` function of the string library looks for the first match of a pattern in a string. If it finds an occurrence of the pattern in the string, it returns the indices in the string (integers representing the position of characters in the string starting from the first character, which is at position 1) where the occurrence starts and ends. If it doesn't find an occurrence of the pattern, it returns nothing. The first parameter it accepts is the string, the second being the pattern and the third being an integer indicating the character position where the `find` function should start searching. Finally, the `find` function can be told to perform a simple match without patterns by being given the value `true` as its fourth argument. It will then simply search for an occurrence of the second string it is given in the first string. The third argument must be given when a simple match is performed. This example code searches for the word "lazy" in a sentence and prints the start and end positions of the occurrence it finds of the word:

```lua
local start_position, end_position = string.find("The quick brown fox jumps over the lazy dog.", "lazy", 1, true)
print("The word \"lazy\" was found starting at position " .. start_position .. " and ending at position " .. end_position .. ".")
```

このコードでは「lazy」という単語は、位置36で始まり、位置39で終わることがわかりました。これは次と同等です。

This code gives the result The word "lazy" was found starting at position 36 and ending at position 39.. It is equivalent to the following:

```lua
local sentence = "The quick brown fox jumps over the lazy dog."
local start_position, end_position = sentence:find("lazy", 1, true)
print("The word \"lazy\" was found starting at position " .. start_position .. " and ending at position " .. end_position .. ".")
```

これは、文字列の `index`メタメソッドが文字列ライブラリの関数を含むテーブルに設定され、 `string.a(b, ...)`を`b:a(...)`に置き換えることができるために機能します 。

This works because the `index` metamethod of strings is set to the table containing the functions of the string library, making it possible to replace `string.a(b, ...)` by `b:a(...)`.

文字の位置を示すインデックスを受け入れる、またはそのようなインデックスを返す文字列ライブラリ内の関数は、最初の文字が位置1にあると見なします。最後の文字が位置-1で、文字列の末尾から逆方向にインデックスを付けます。

Functions in the string library that accept indices to indicate character position or that return such indices consider the first character as being at position 1. They accept negative numbers and interpret them as indexing backwards, from the end of the string, with the last character being at position -1.

パターンは、文字列が一致するかどうかを示す特定の表記法に従う文字列です。この目的のために、パターンには文字クラス、つまり文字のセットを表す組み合わせが含まれています。

Patterns are strings that follow a certain notation to indicate a pattern that a string may match or not. For this purpose, patterns contain character classes, combinations that represent sets of characters.

| 文字の組み合わせ | 説明                                 |
| ---------------- | ------------------------------------ |
| .                | すべての文字                         |
| %a               | 文字（大文字と小文字）               |
| %c              | 制御文字                             |
| %d              | 数字                                 |
| %g             | 印刷可能な文字（スペース文字を除く） |
| %l           | 小文字                               |
| %p               | 句読文字                             |
| %s               | スペース文字                         |
| %u               | 大文字                               |
| %w               | 英数字（数字と文字）                 |
| %x               | 16進数                               |

| Character combination | Description                                       |
| --------------------- | ------------------------------------------------- |
| .                     | All characters                                    |
| %a                    | Letters (uppercase and lowercase)                 |
| %c                    | Control characters                                |
| %d                    | Digits                                            |
| %g                    | Printable characters (except the space character) |
| %l                    | Lowercase letters                                 |
| %p                    | Punctuation characters                            |
| %s                    | Space characters                                  |
| %u                    | Uppercase letters                                 |
| %w                    | Alphanumeric characters (digits and letters)      |
| %x                    | Hexadecimal digits                                |

特殊ではないすべての文字はそれ自体を表し、特殊文字（英数字ではないすべての文字）は、パーセント記号を接頭辞として付けることでエスケープできます。 キャラクタークラスを組み合わせて、セットに入れることで、より大きなキャラクタークラスを作成できます。 セットは、角括弧で囲まれた文字クラスとして示されます（つまり、 `[％xp]`は、すべての16進文字と文字「p」のセットです）。 文字の範囲は、範囲の終了文字をハイフンで昇順で区切ることで確認できます（つまり、 `[0-9％s]`は0から9までのすべての数字とスペース文字を表します）。キャレット（ "^"）文字がセットの先頭（開始角括弧の直後）に配置されている場合、セットには、キャレットがセットの先頭に配置されていなかった場合に含まれていた文字を除くすべての文字が含まれます。

All characters that are not special represent themselves and special characters (all characters that are not alphanumeric) can be escaped by being prefixed by a percentage sign. Character classes can be combined to create bigger character classes by being put in a set. Sets are noted as character classes noted between square brackets (i.e. `[%xp]` is the set of all hexadecimal characters plus the letter "p"). Ranges of characters can be noted by separating the end characters of the range, in ascending order, with a hyphen (i.e. `[0-9%s]` represents all the digits from 0 to 9 plus space characters). If the caret ("^") character is put at the start of the set (right after the opening square bracket), the set will contain all characters except those it would have contained if that caret had not been put at the start of the set.

パーセント記号 `%` の前にある文字で表されるすべてのクラスの補数は、パーセント記号の後に対応する大文字が続くものとして示されます（つまり、 `%S` はスペース文字を除くすべての文字を表します）。

The complement of all classes represented by a letter preceded of a percentage sign can be noted as a percentage sign followed by the corresponding uppercase letter (i.e. `%S` represents all characters except space characters).

パターンは、文字列がそれに一致するためにパターン内でどのシーケンスを見つける必要があるかを表すパターンアイテムのシーケンスです。 パターンアイテムは、文字クラスにすることができます。この場合、クラス内の任意の文字に1回一致し、文字クラスの後に「`*`」文字が続きます。この場合、クラス内の文字の0回以上の繰り返しに一致します（これら 繰り返し項目は常に可能な限り長いシーケンスに一致します）、文字クラスの後に追加（ 「`+`」）文字が続きます。この場合、クラス内の文字の1つ以上の繰り返しに一致します（これらの繰り返し項目も常に可能な限り長いものに一致します） シーケンス）、文字クラスの後にマイナス（ 「`-`」）文字が続きます。この場合、クラス内の文字の0回以上の繰り返しに一致しますが、最も短いシーケンスまたは文字クラスとそれに続く疑問符に一致します。この場合、クラス内の文字の1つまたは出現なしに一致します。

Patterns are sequences of pattern items that represent what sequences should be found in the pattern for a string to match it. A pattern item can be a character class, in which case it matches any of the characters in the class once, a character class followed by the "*" character, in which case it matches 0 or more repetitions of characters in the class (these repetition items will always match the longest possible sequence), a character class followed by the addition ("+") character, in which case it matches 1 or more repetitions of characters in the class (these repetition items will also always match the longest possible sequence), a character class followed by the minus ("-") character, in which case it matches 0 or more repetitions of characters in the class, but matches the shortest possible sequence or a character class followed by an interrogation mark, in which case it matches one or no occurrence of a character in the class.

以前にキャプチャされた部分文字列と同等の部分文字列を一致させることができます。`%1`は最初にキャプチャされた部分文字列と一致し、 `%2`は2番目の部分文字列と一致し、以下同様に`%9`まで続きます。 キャプチャについては、以下で説明します。 リファレンスマニュアルで説明されているように、パターンによって提供される他の2つの機能があります。

It is possible to match substrings equivalent to previously captured substrings: `%1` will match the first captured substring, `%2` the second, and so on until `%9`. Captures are described below. There are two other functionalities offered by patterns, as described by the reference manual:

> `%bxy`、ここでxとyは2つの異なる文字です。 このような項目は、xで始まり、yで終わり、xとyのバランスが取れている文字列に一致します。 つまり、文字列を左から右に読み、xの場合は + 1、yの場合は-1を数えると、最後のyは、数が0に達する最初のyになります。たとえば、項目 `%b()`は バランスの取れた括弧で式を照合します。
>
> `%f[set]`、フロンティアパターン。 このような項目は、次の文字がセットに属し、前の文字がセットに属さないように、任意の位置で空の文字列と一致します。 セットセットは、前述のように解釈されます。 件名の最初と最後は、文字「 '\0'」であるかのように処理されます。
>
> —Lua authors, [Lua 5.2 Reference Manual](http://www.lua.org/manual/5.2/manual.html#6.4.1)



> `%bxy`, where x and y are two distinct characters; such item matches strings that start with x, end with y, and where the x and y are balanced. This means that, if one reads the string from left to right, counting +1 for an x and -1 for a y, the ending y is the first y where the count reaches 0. For instance, the item `%b()` matches expressions with balanced parentheses.
>
> `%f[set]`, a frontier pattern; such item matches an empty string at any position such that the next character belongs to set and the previous character does not belong to set. The set set is interpreted as previously described. The beginning and the end of the subject are handled as if they were the character '\0'.
>
> —Lua authors, [Lua 5.2 Reference Manual](http://www.lua.org/manual/5.2/manual.html#6.4.1)

パターンはパターン項目のシーケンスであり、オプションでキャレット`^`が前に付き、パターンが文字列の先頭でのみ一致できることを示し、オプションでドル記号`$`が続きます。これは、パターンが文字列の最後でのみ一致できることを示します 。 これらの記号は、文字列の最初または最後に一致を固定すると言われています。 これらの2つの文字は、パターンの最初または最後にある場合にのみ特別な意味を持ちます。

Patterns are sequences of pattern items, optionally preceded by a caret, which indicates that the pattern can only match at the beginning of the string, and optionally followed by a dollar sign, which indicates that the pattern can only match at the end of the string. These symbols are said to anchor the match at the beginning or the end of the string. These two characters only have a special meaning when at the beginning or at the end of a pattern.



サブパターンは、キャプチャを示すためにパターン内の括弧で囲むことができます。一致が成功すると、キャプチャに一致する文字列の部分文字列は、将来使用するために保存されます。たとえば、`gmatch`によって返されます。常に左括弧の位置から番号が付けられます。 2つの空の括弧は、現在の文字列位置（数値であり、文字列の一部ではありません）をキャプチャする空のキャプチャを示します。



Sub-patterns can be enclosed inside parentheses inside patterns to indicate captures. When a match succeeds, the substrings of the string that match captures are stored for future use, for example to be returned by `gmatch`. They are always numbered starting from the position of their left parenthesis. Two empty parentheses denote the empty capture, which captures the current string position (which is a number and is not a part of the string).



この`gmatch`関数を使用して、文字列内のパターンの出現を反復処理できます。`find`関数とは異なり、検索を開始する初期位置を指定したり、単純なマッチングを実行したりすることはできません。この`gmatch`関数は、呼び出されると、文字列内の指定されたパターンから次のキャプチャを返すイテレータを返します。パターンにキャプチャが指定されていない場合は、代わりに一致全体が示されます。次の例は、文中の単語を反復処理して1つずつプリントする方法を示しています。



The `gmatch` function can be used to iterate through the occurrences of a pattern in a string; it is not possible, unlike with the `find` function, to specify an initial position to start searching or to perform simple matching. The `gmatch` function returns an iterator that, when called, returns the next captures from the given pattern in the string. The whole match is given instead if there are no captures specified in the pattern. The following example shows how to iterate through the words in a sentence and print them one by one:

```lua
local sentence = "The quick brown fox jumps over the lazy dog."
for word in sentence:gmatch('%a+') do
	print(word)
end
```

この例では、一致全体は、イテレータであるwordによって返される唯一の値によって与えられます。

`gsub`関数を使用して、文字列内のパターンのすべての出現箇所を別のものに置き換えることができます。 最初の2つの引数は文字列とパターンで、3番目はオカレンスを置き換える文字列で、4番目は置き換える必要のあるオカレンスの最大数です。 3番目の引数は、文字列ではなく、テーブルまたは関数にすることもできます。

In this example, the entire match is given by the only value returned by the iterator, word.

The `gsub` function can be used to replace all occurrences of a pattern in a string by something else. Its first two arguments are the string and the pattern, while the third is the string to replace occurrences by and the fourth is the maximum number of occurrences that should be replaced. The third argument, instead of being a string, can also be a table or a function.

3番目の引数が文字列の場合、それは置換文字列と呼ばれ、文字列内のパターンの出現を置換します。 パターンによって保存されたキャプチャは、置換文字列に埋め込むことができます。 それらは、キャプチャの数を表す数字が続くパーセント記号によって示されます。 一致自体は `%0`で表すことができます。 置換文字列のパーセント記号は、 `%%`としてエスケープする必要があります。

When the third argument is a string, it is called the replacement string and it replaces occurrences of the pattern in the string. Captures stored by the pattern can be embedded in the replacement string; they are noted by a percentage sign followed by a digit representing the number of the capture. The match itself can be represented by `%0`. Percentage signs in replacement strings must be escaped as `%%`.

3番目の引数がテーブルの場合、最初のキャプチャはそのテーブルにインデックスを付けるためのキーとして使用され、置換文字列はテーブル内のそのキーに対応する値です。 関数の場合、その関数は一致するたびに呼び出され、すべてのキャプチャが引数として渡されます。 どちらの場合も、キャプチャがない場合は、代わりに一致全体が使用されます。 関数またはテーブルの値が `false`または` nil`の場合、置換は行われません。

When the third argument is a table, the first capture is used as a key to index that table and the replacement string is the value corresponding to that key in the table. When it is a function, that function is called for every match, with all captures passed as arguments. In both cases, if there is no capture, the entire match is used instead. If the function or table gives the value `false` or `nil`, no replacement is done.

Lua 5.2リファレンスマニュアルから直接引用したいくつかの例を次に示します。
Here are some examples taken directly from the Lua 5.2 Reference Manual:

> ```lua
> x = string.gsub("hello world", "(%w+)", "%1 %1")
> --> x="hello hello world world"
> 
> x = string.gsub("hello world", "%w+", "%0 %0", 1)
> --> x="hello hello world"
> 
> x = string.gsub("hello world from Lua", "(%w+)%s*(%w+)", "%2 %1")
> --> x="world hello Lua from"
> 
> x = string.gsub("home = $HOME, user = $USER", "%$(%w+)", os.getenv)
> --> x="home = /home/roberto, user = roberto"
> 
> x = string.gsub("4+5 = $return 4+5$", "%$(.-)%$", function (s)
>       return load(s)()
>     end)
> --> x="4+5 = 9"
> 
> local t = {name="lua", version="5.2"}
> x = string.gsub("$name-$version.tar.gz", "%$(%w+)", t)
> --> x="lua-5.2.tar.gz"
> ```
>
> —Lua authors, [Lua 5.2 Reference Manual](http://www.lua.org/manual/5.2/manual.html#6.4.1)

Luaは、パターンマッチング以外の文字列操作機能を提供します。 これらには、文字の順序を逆にして文字列を返す `reverse`関数、文字列に相当する小文字を返す` lower`関数、文字列に相当する大文字を返す `upper`関数が含まれます。 文字列の長さを返す `len`関数と、引数として指定された2つの文字位置で開始および終了する文字列の部分文字列を返す` sub`関数。 他にもあり、それらのドキュメントはLua 5.2リファレンスマニュアルにあります。

Lua offers other functions for manipulating strings than those for pattern matching. These include the `reverse` function, which returns a string with the order of the characters reversed, the `lower` function, which returns the lowercase equivalent of a string, the `upper` function, which returns the uppercase equivalent of a string, the `len` function, which returns the length of a string and the `sub` function, which returns the substring of a string that starts at and ends at the two character positions given as arguments. There are more, and their documentation can be found in the Lua 5.2 Reference Manual.

1. [↑](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_ref-3) [Ierusalimschy, Roberto](https://en.wikipedia.org/wiki/Roberto_Ierusalimschy); Celes, Waldemar; Henrique de Figueiredo, Luiz. [*Lua 5.2 Reference Manual*](http://www.lua.org/manual/5.2). http://www.lua.org/manual/5.2. Retrieved 30 November 2013.
2. [↑](https://en.m.wikibooks.org/wiki/Lua_Programming/Print_version#cite_ref-4) Functions that were already described elsewhere will not be described in this chapter.



# Appendix:Software testing

The term **software testing** refers to a number of methods and processes that are used to discover bugs and programming mistakes in computer software. Software testing can be done statically, in which case in is called static testing and is done without executing the computer software, or dynamically, in which case it is called dynamic testing and is done while the computer program that is being tested is running.

## Type checking

> In programming languages, a **type system** is a collection of rules that assign a property called a *[type](https://en.wikipedia.org/wiki/type_(computer_science))* to the various constructs—such as [variables](https://en.wikipedia.org/wiki/variable_(computer_science)), [expressions](https://en.wikipedia.org/wiki/expression_(computer_science)), [functions](https://en.wikipedia.org/wiki/function_(computer_science)) or [modules](https://en.wikipedia.org/wiki/modular_programming)—a [computer program](https://en.wikipedia.org/wiki/computer_program) is composed of. The main purpose of a type system is to reduce [bugs](https://en.wikipedia.org/wiki/bug_(computer_programming)) in computer programs by defining interfaces between different parts of a computer program, and then checking that the parts have been connected in a consistent way. This checking can happen statically (at [compile time](https://en.wikipedia.org/wiki/compile_time)), dynamically (at [run time](https://en.wikipedia.org/wiki/run_time_(program_lifecycle_phase))), or it can happen as a combination of static and dynamic checking. Type systems have other purposes as well, such as enabling certain compiler optimizations, allowing for [multiple dispatch](https://en.wikipedia.org/wiki/multiple_dispatch), providing a form of documentation, etc.
>
> —Wikipedia, [Type system](https://en.wikipedia.org/wiki/Type_system)

Type-checking can be done, as the extract from Wikipedia brilliantly said, at run time or at compile time. If it is done at compile time, the compiler, when compiling source code, will verify the type safety of the program and guarantee that the program satisfies certain type safety properties—generally, static type-checkers will simply verify that variables always have values of the same type and that arguments passed to functions will have the right type.

The static approach allows bugs to be discovered early in the development cycle. The dynamic approach, in contrast, consists in verifying that the program follows the type constraints when it is running. While this means that dynamic type-checkers should be able to verify more constraints, most dynamically typed languages do not have many type constraints. Lua is a dynamically typed language: in Lua, values have types, but variables do not. This means that the value of a variable can be a number at some point of the program’s execution and be a string at another point.

Lua’s type system is very simple in comparison with most other languages. It performs type checking when operators are used (attempting to add two values of which at least one is not a number and cannot be coerced to one, for example, will raise a type error) and when functions of the standard libraries are called (functions of the standard library reject arguments that do not have the right type and raise an appropriate error).

Since Lua does not have functionality for specifying a type for function parameters, the `type` function can be useful to verify that arguments passed to functions are of the appropriate type. This is most useful for functions that will be passed arguments provided by users while a program is running (for example, in an interactive environment for calling predefined Lua functions), since adding code for type checking to functions makes them more verbose and adds maintenance overhead.

## White-box testing

The term white-box testing refers to the practice of using knowledge of the internal workings of software to create test cases to verify its functionality. It is relevant at three levels of software testing, but the one most interesting for Lua programs is the unit level, since Lua programs are usually part of a bigger application where the integration and system testing would take place.

There are multiple frameworks available for unit testing in Lua. Testing at the unit level is most appropriate for libraries, since it generally consists in writing test cases that pass specific arguments to functions and provide a warning when a function returns an unexpected value. This requires writing test cases for new functionality, but has the benefit of making errors introduced in code easier to notice when they modify the behavior of functions in a way that makes the tests not pass anymore.

There are multiple unit testing frameworks for Lua. One of them, busted, supports the standard Lua virtual machine as well as LuaJIT, and can also be used with MoonScript and Terra, the former a language that compiles to Lua and the latter a low-level language that is interoperable with Lua. Another unit testing framework for Lua, Luaunit, is written entirely in Lua and has no dependencies. Shake is a simpler test framework, initially part of the Kepler Project, that uses the `assert` and `print` functions but is no longer actively developed.

## Further reading

The lua-users wiki, an excellent resource to find information about Lua, provides the following material that is related to software testing. Some of these pages consist in links to other pages or to projects that can be useful for various tasks.

- [Lua Type Checking](http://lua-users.org/wiki/LuaTypeChecking)
- [Unit Testing](http://lua-users.org/wiki/UnitTesting)
- [Debugging Lua Code](http://lua-users.org/wiki/DebuggingLuaCode)
- [Program Analysis](http://lua-users.org/wiki/ProgramAnalysis)
- [Debugging and Testing](http://lua-users.org/wiki/DebuggingAndTesting)

# Glossary

This is a glossary that contains terms related to programming in the context of Lua. Its use is recommended to find the meaning of words that are not understood.

- abstract class

  An [abstract class](https://en.wikipedia.org/wiki/concrete_class#Abstract_and_concrete) is a class of which instances cannot be created directly. Abstract classes are [abstract types](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#abstract_type).

- abstract data type

  An [abstract data type](https://en.wikipedia.org/wiki/abstract_data_type) is a model to represent a class of [data structures](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#data_structure) that have similar behavior. Abstract data types are defined by the operations that can be performed on them and by mathematical constraints of these operations rather than by the implementation and the way the data is stored in the memory of the computer.

- abstract type

  An [abstract type](https://en.wikipedia.org/wiki/abstract_type) is a type of data of which instances cannot be created directly.

- actual parameter

  See [argument](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#argument).

- additive inverse

  The [additive inverse](https://en.wikipedia.org/wiki/additive_inverse) of a number is the number that, when added to that number, yields zero. For example, the additive inverse of 42 is -42.

- arithmetic negation

  Arithmetic negation is the operation that produces the [additive inverse](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#additive_inverse) of a number.

- arithmetic operation

  An [arithmetic operation](https://en.wikipedia.org/wiki/arithmetic_operation) is an operation whose operands are numbers.

- arity

  The [arity](https://en.wikipedia.org/wiki/arity) of an operation or of a function is the number of operands or arguments the operation or function accepts.

- argument

  An [argument](https://en.wikipedia.org/wiki/parameter_(computer_programming)) is a value passed to a [function](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#function).

- array

  An [array](https://en.wikipedia.org/wiki/array_data_structure) is a [data structure](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#data_structure) consisting of a collection of values, each identified by at least one array index or key.

- associative array

  An [associative array](https://en.wikipedia.org/wiki/associative_array) is an [abstract data type](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#abstract_data_type) composed of a collection of pairs of keys and values, such that each possible key appears at most once in the collection.

- augmented assignment

  [Augmented assignment](https://en.wikipedia.org/wiki/Augmented_assignment) is a type of assignment that gives a variable a value that is relative to its prior value.

- binary operation

  A [binary operation](https://en.wikipedia.org/wiki/binary_operation) is an operation of which the arity is two.

- boolean

  See [logical data](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#logical_data).

- boolean negation

  See [logical negation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#logical_negation).

- chained assignment

  [Chained assignment](https://en.wikipedia.org/wiki/Chained_assignment) is a type of assignment that gives a single value to many variables. Example: `a = b = c = d = 0`.

- chunk

  A chunk is a sequence of statements.

- compound assignment

  See [augmented assignment](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#augmented_assignment).

- concatenation

  [String concatenation](https://en.wikipedia.org/wiki/String_concatenation) is the operation of joining two strings of characters. For example, the concatenation of "snow" and "ball" is "snowball".

- concrete class

  A concrete class is a class of which instances can be created directly. Concrete classes are [concrete types](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#concrete_type).

- concrete type

  A concrete type is a type of which instances can be created directly.

- condition

  A condition is a [predicate](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#predicate) that is used in a [conditional statement](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#conditional_statement) or as an operand to the [conditional operator](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#conditional_operator). Conditions, in Lua, are considered as true when their expression evaluates to a value other than `nil` or `false`, and are considered as false otherwise.

- conditional operator

  A [conditional operator](https://en.wikipedia.org/wiki/conditional_operator) is an operator that returns a value if a [condition](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#condition) is true and another if it isn't.

- conditional statement

  A [conditional statement](https://en.wikipedia.org/wiki/conditional_(computer_programming)) is a statement that executes a piece of code if a [condition](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#condition) is true.

- data structure

  A [data structure](https://en.wikipedia.org/wiki/data_structure) is a particular way of storing and organizing data in the memory of a computer. It is the implementation of an [abstract data type](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#abstract_data_type).

- data type

  A [data type](https://en.wikipedia.org/wiki/data_type) is a model for representing the storage of data in the memory of a computer.

- dictionary

  See [associative array](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#associative_array).

- exclusive disjunction

  [![img](https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Venn0110.svg/110px-Venn0110.svg.png)](https://en.m.wikibooks.org/wiki/File:Venn0110.svg)[Venn diagram](https://en.wikipedia.org/wiki/Venn_diagram) of {\displaystyle \scriptstyle a\veebar b}![\scriptstyle a\veebar b](https://wikimedia.org/api/rest_v1/media/math/render/svg/a52d88abb3e9486cf9fcd53b50c0fcaf3a621f32)The [exclusive disjunction](https://en.wikipedia.org/wiki/exclusive_or) operation is a [binary operation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#binary_operation) that produces the value `true` when one of its operands is true but the other is not. The exclusive disjunction of a and b is expressed mathematically as {\displaystyle \scriptstyle a\veebar b}![\scriptstyle a\veebar b](https://wikimedia.org/api/rest_v1/media/math/render/svg/a52d88abb3e9486cf9fcd53b50c0fcaf3a621f32). There is no operator corresponding to exclusive disjunction in Lua, but {\displaystyle \scriptstyle a\veebar b}![\scriptstyle a\veebar b](https://wikimedia.org/api/rest_v1/media/math/render/svg/a52d88abb3e9486cf9fcd53b50c0fcaf3a621f32) can be represented as `(a or b) and not (a and b)`.

- formal parameter

  See [parameter](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#parameter).

- function

  A function is a sequence of statements (instructions) that perform a specific task. Functions can be used in a program wherever that particular task needs to be performed. Functions are usually defined in the program that will use them, but are sometimes defined in libraries that can be used by other programs.

- hash map

  See [hash table](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#hash_table).

- hash table

  A [hash table](https://en.wikipedia.org/wiki/hash_table) is an implementation as a [data structure](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#data_structure) of the [associative array](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#associative_array). A hash table uses a [hash function](https://en.wikipedia.org/wiki/hash_function) to compute an index into an array of buckets or slots, from which the value corresponding to the index can be found.

- inline if

  See [conditional operator](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#conditional_operator).

- integer

  An [integer](https://en.wikipedia.org/wiki/integer) is a number that can be written without a fractional or decimal component. Integers are implemented in Lua in the same way as other numbers.

- length operation

  The length operation is the operation that produces the number of values in an array.

- literal

  A literal is a notation for representing a fixed value in source code. All values can be represented as literals in Lua except threads and userdata.

- logical complement

  The [logical complement](https://en.wikipedia.org/wiki/logical_complement) of a boolean value is the boolean value that is not that value. This means the logical complement of `true` is `false` and vice versa.

- logical conjunction

  [![img](https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Venn0001.svg/110px-Venn0001.svg.png)](https://en.m.wikibooks.org/wiki/File:Venn0001.svg)Venn diagram of {\displaystyle \scriptstyle a\land b}![{\displaystyle \scriptstyle a\land b}](https://wikimedia.org/api/rest_v1/media/math/render/svg/60d14811b3ea72e1c7f806e4d3b71eb03a1c532c)The [logical conjunction](https://en.wikipedia.org/wiki/logical_conjunction) operation is a [binary operation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#binary_operation) that produces the value `true` when both of its operands are true and `false` in all other cases. It is implemented as the `and` operator in Lua and it returns its first operand if it is `false` or `nil` and the second operand otherwise. The logical conjunction of a and b is expressed mathematically as {\displaystyle \scriptstyle a\land b}![{\displaystyle \scriptstyle a\land b}](https://wikimedia.org/api/rest_v1/media/math/render/svg/60d14811b3ea72e1c7f806e4d3b71eb03a1c532c).

- logical data

  The [logical data type](https://en.wikipedia.org/wiki/logical_data_type), which is generally called the boolean type, is the type of the values `false` and `true`.

- logical disjunction

  [![img](https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Venn0111.svg/110px-Venn0111.svg.png)](https://en.m.wikibooks.org/wiki/File:Venn0111.svg)Venn diagram of {\displaystyle \scriptstyle a\lor b}![{\displaystyle \scriptstyle a\lor b}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ceea040fb1a260ea93318775c6b3c643e2964f9f)The [logical disjunction](https://en.wikipedia.org/wiki/logical_disjunction) operation is a [binary operation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#binary_operation) that produces the value `false` when both of its operands are false and `true` in all other cases. It is implemented as the `or` operator in Lua and it returns the first operand if it is neither `false` nor `nil` and the second otherwise. The logical disjunction of a and b is expressed mathematically as {\displaystyle \scriptstyle a\lor b}![{\displaystyle \scriptstyle a\lor b}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ceea040fb1a260ea93318775c6b3c643e2964f9f).

- logical negation

  [Logical negation](https://en.wikipedia.org/wiki/Logical_negation), implemented in Lua by the `not` operator, is the operation that produces the [logical complement](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#logical_complement) of a boolean value.

- map

  See [associative array](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#associative_array).

- method

  A [method](https://en.wikipedia.org/wiki/method_(computer_programming)) is a function that is a member of an object and generally operates on that object.

- modulo

  See [modulo operation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#modulo_operation).

- modulo operation

  The [modulo operation](https://en.wikipedia.org/wiki/modulo_operation), implemented in Lua by the `%` operator, is the operation that produces the remainder of the division of a number by another.

- modulus

  See [modulo operation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#modulo_operation).

- multiple assignment

  See [parallel assignment](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#parallel_assignment).

- nil

  The type nil is the type of the value `nil`, whose main property is to be different from any other value; it usually represents the absence of a useful value.

- not operator

  See [logical negation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#logical_negation).

- number

  The number type represents real ([double-precision floating-point](https://en.wikipedia.org/wiki/double-precision_floating-point)) numbers. It is possible to build Lua interpreters that use other internal representations for numbers, such as single-precision float or long integers.

- operator

  An [operator](https://en.wikipedia.org/wiki/operator_(computer_programming)) is a token that generates a value from one or many operands.

- parallel assignment

  [Parallel assignment](https://en.wikipedia.org/wiki/Parallel_assignment) is a type of assignment that simultaneously assigns values to different variables.

- parameter

  A [parameter](https://en.wikipedia.org/wiki/parameter_(computer_programming)) is a variable in a function definition to which the argument that corresponds to it in a call to that function is assigned.

- predicate

  A predicate is an expression that evaluates to a piece of [logical data](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#logical_data).

- procedure

  See [function](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#function).

- relational operator

  A [relational operator](https://en.wikipedia.org/wiki/relational_operator) is an operator that is used to compare values.

- routine

  See [function](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#function).

- sign change

  See [arithmetic negation](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#arithmetic_negation).

- simultaneous assignment

  See [parallel assignment](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#parallel_assignment).

- string

  The type string represents arrays of characters. Lua is 8-bit clean: strings can contain any 8-bit character, including embedded zeros.

- string literal

  A [string literal](https://en.wikipedia.org/wiki/string_literal) is the representation of a string value within the source code of a computer program. With respect to syntax, a string literal is an expression that evaluates to a string.

- subprogram

  See [function](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#function).

- subroutine

  See [function](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#function).

- symbol

  See [token](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#token).

- symbol table

  A [symbol table](https://en.wikipedia.org/wiki/symbol_table) is an implementation as a [data structure](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#data_structure) of the [associative array](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#associative_array). They are commonly implemented as [hash tables](https://en.m.wikibooks.org/wiki/Lua_Programming/Glossary#hash_table).

- token

  A token is an atomic piece of data, such as a word in a human language or such as a keyword in a programming language, for which a meaning may be inferred during parsing.

- variable

  A [variable](https://en.wikipedia.org/wiki/variable_(computer_science)) is a label associated to a location in the memory. The data in that location can be changed and the variable will point to the new data.

- variadic function

  A [variadic function](https://en.wikipedia.org/wiki/variadic_function) is a function of indefinite arity.
