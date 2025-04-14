# direct-input23 デモ
 
別リポジトリで公開している direct-input23.ahk の紹介用デモリポジトリです。

direct-input23.ahk の詳細については、[元リポジトリ](https://github.com/kouie/direct-input23)の Readme をご覧ください。

## 動作環境

Windows 11 ＋ Chrome ブラウザで動作確認しております。

## デモサイトの使い方

サイトには、「姓名 (漢字)」、「姓名 (カタカナ)」、「チュートリアル」、「ゲーム」の 4 つのタブが表示されます。

まずは、「チュートリアル」で基本的な入力方法をご確認ください (すぐ終わります)。そのあと、「姓名 (漢字)」タブと「姓名 (カタカナ)」タブで、「変換キーを使用しない入力」の具合をお試しください。

デフォルト状態で「姓名 (漢字)」タブで使用している漢字辞書は、再変換があまり発生しないように調整してあります。再変換機能を試してみたい場合は、「姓名 (カタカナ)」タブで入力してみてください。カタカナ辞書はほとんど調整していませんので、画面の読みに従って入力した場合に結構な頻度で再変換が必要になります。

独自の辞書や課題を試してみたい場合は、下部の「設定」セクションでデータをロードできます。辞書ファイルの仕様・形式については、元リポジトリの情報や本リポジトリの dat フォルダ (dictionary-local.txt と dictionary-kana.txt) を参考にしてください。課題データは、入力対象を 1 行に 1 題ずつ記述する形式です (dat フォルダの names.txt を参考にしてください)。読みのデータは選択中の辞書から自動的に取得されます。どちらのデータも、BOM 付 UTF-8、CRLF 形式で作成してください (元リポジトリでそのまま使用できます)。読み込んだ辞書はドロップダウンメニューに、課題データは上部のタブにそれぞれ追加されます。

メモ： 辞書に登録されていない漢字が含まれている課題はクリアできませんので、その場合は F2 キーで先に進めてください。

「ゲーム」タブは昔あった電卓風のゲームです。漢字 (敵機) の列が表示領域の左端に到達する前に、対応する読みを入力して (攻撃して) 敵機を撃墜してください。攻撃の判定 (入力した漢字が一致するかどうか) は常に列の先頭に対して行われ、画面の右側で成功した攻撃ほど点数が高くなります。ゲームスタート時は 1 文字ずつしか攻撃できませんが、ステージをクリアしていくと撃てる (入力できる) 読みが追加されていき、連続する 2 文字の漢字ペアを消せるようになります (1 文字ずつでも消せますが、まとめて消すと 2 文字目のスコアが 2 倍になります)。攻撃可能な漢字ペアが揃えば、ペアの読みを優先して表示するようになっています。ステージ開始の時点で画面外に敵が 2 機いますので高得点を狙 (文章はここで途絶えている)。

「ゲーム」タブは、本デモサイトで使用している入力チェック機能を紹介するデモを兼ねていて、入力対象の動的な生成や条件に応じた表示内容の分岐などを、課題データに JSON (風) のデータを追加することで制御しています (いまのところはテスト版で、「設定」セクションはこの形式のデータファイルの読み込みに対応していません)。興味がある方は dat フォルダの invade.txt ファイルをご覧ください (手打ちです)。

## データについて

このリポジトリには人名を表すデータが多数含まれていますが、いずれも架空のものであり、実在の人物とは一切関係ありません。

## 免責事項

当ソフトウェアの使用に関連して生じたいかなる損害、損失、またはトラブルについても、一切の責任を負いません。これには、データの損失、収益の損失、ビジネスの中断、およびその他の金銭的損失が含まれますが、これに限られません。

## ライセンスについて

このデモサイトおよびそのコードは非商用目的でのみ利用可能です。詳細については、[LICENSE ファイル](./LICENSE)を参照してください (元になる direct-input23.ahk のリポジトリとライセンスの扱いが異なりますのでご注意ください)。
