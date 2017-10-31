#ブロックの作成

ブロックは、ファッションの最も重要な部分の1つであり、一部の主要部分です。 
外観と品質から
ブロックは強く依存し、一般的にはmodの品質に依存します。
ブロックを作成するには、ブロックを与える必要があります
テクスチャ、ID、名前、プロパティ、およびその他の重要なパラメータについては、これを行う方法は以下のとおりです。
ユニークなadiの生成
ID - ブロックの一意の識別子。文字列と自然数で与えられます。
この文字列と一致します。 IDを登録するには、IDRegistryモジュールが使用されます。 の
ブロックIDの登録には次の方法が使用されます。
IDRegistry.genBlockID("String_ID") - この関数を呼び出した後、新しいブロックの一意のID。 
このブロックのidiを使用するためには、BlockIDを使用します。 String_ID - ブロックのIDを返します。

テクスチャ
リソースモードでは、ブロックとオブジェクトのテクスチャは特定の形式で指定されます。各テクスチャ.png形式で、名前と番号が必要です。 
テクスチャの名前は次のようになります。name_number.png など。 同じ名前のテクスチャ番号は順番に移動する必要があります。
始まる
と
0。
テクスチャ
ブロック
の
リソース
位置している
〜に
アドレス
your_ext_package / terrain-atlas /
ブロックの作成
ブロックのIDを登録したら、そのIDでブロックを作成する必要があります。 1つのIDは
ブロックのいくつかのバリエーションが作成され、それぞれに独自の名前とテクスチャがあり、
世界の1つのブロックの異なるバリエーションは1つのIDを持ちますが、メタデータの値は異なります。 の
ブロックモジュールを使用したブロックの作成。
Block.createBlock （ "string ID"、[ Variance_1 、 variation_2 、...]、 特殊ブロックタイプ ） - 作成する
以前に登録されたIDのすべてのバリエーションをブロックします。 配列内の各バリエーションは
フォーマット：
{名前： "バリエーション名"、テクスチャ：[["texture_1"、<テクスチャ番号1]]、["texture_2"、<number
テクスチャ_3]、[テクスチャ_3]、[テクスチャ_4]、<テクスチャ_4>]、
["texture_5"、<texture_number_5>]、["texture_6"、<texture_number_6>]、inCreative：true / false
（このバリエーションをクリエイティブに追加するかどうか）} テクスチャが6未満の場合は、
それらの最後のものは、数を6に補うために何度も複製されます。最初のもの
配列の要素は 底部 、2番目は上部 、3番目は北部 、4番目は南部 、5は東部 、6は西部です。
Page 2
したがって、ブロックのすべての面で同じテクスチャコードを以下に減らすことができます。
{名前： "バリエーション名"、テクスチャ：[["texture_1"、<テクスチャ番号1]]、inCreative：true / false}
場合によっては、メカニズムを作成するために、回転を含むブロックを作成する必要があります。 内部でこれを行うには
コアにはメソッドもあります：
Block.createBlockWithRotation （ "文字列ID"、[ Variance_1 、 variation_2 、...]） - 同じものを取ります
引数は Block.createBlock として 扱われますが、ブロックのバリエーションごとに4つのバリエーションが作成されます
回転を実現すると、この方法で作成されたブロックは自動的に目的の
ターン。
特殊タイプ
標準（グロー、モデル）とは異なるパラメータでブロックを作成するには、
特別な種類のブロックが使用されます。 それらは関数を使用して登録されます
Block.createSpecialType （ フィーチャオブジェクト ） - この関数は、
これらの特性を持つ特殊なタイプのブロックを変更して与える必要があります。 1つの特別なタイプ
さまざまなブロックの合計128個のバリエーションで作成できます。
すべての特性、デフォルト値、およびその説明：
{
base：20、ブロックの作成の基礎となるMCPEからのブロックは、
いくつかの特性と材料がコピーされた
不透明：false、 - 不透明、trueの場合、mobはブロック内にダメージを受けます。
このブロックと他のブロックとの接触場所は描画されません
renderlayer：4、レンダリングタイプ、4は透明部分がレンダリングされることを意味します
透明、黒ではない
redstoneconsumer：true、 - redston信号変更イベントがあるかどうか
このユニットの
lightopacity：1、 - 光の不透明度、光が吸収される量
このブロックを通過すると、0 - 完全に透明、15 - 完全に不透明
lightlevel：0、 - ブロックグロー、0 - グローなし、15 - 最大グロー
explosionres：2、 - 防爆
color：[0xFFFFFF] - 0xRRGGBBという形式の各辺の色
}
Page 3
Blockモジュールの残りのメソッド
Block.registerDropFunction （ "文字列ブロックID"、ドロップ関数 ）
ドロップ関数の形式は次のとおりです。
関数（coords、id、data、diggingLevel、toolLevel）{
coords - 破壊されたブロックの座標を含むオブジェクト - {x :, y :, z：} - coords.x、coords.y、
coords.z
id、ブロックのデータIDとデータ、idは常に関数が登録されたものと一致し、
同じ機能が異なるブロックに登録されている場合は、
diggingLevel - ブロックブレークのレベル。別のタイプの手またはツールが0の場合。同じ
ツールがブロックの材質と一致すると、レベルはインストゥルメントのレベルに等しくなります
toolLevel - 手の中のツールのレベルで、ブロック自体に依存しません
ブロックが何かを落とした場合、この関数は、必要な項目の配列を返します。
ドロップすると、各アイテムのフォーマットは[id、count、data]
return [[id、count、data]、[id1、count、data]]
}
Block.registerDropFunctionForID （ 数値ブロックID、ドロップ関数 ） は前の
メソッドではなく、数値IDを引数として使用します。
Block.registerPlaceFunction （ "文字列ブロックID"、インストール関数 ）
インストール機能の形式は次のとおりです。
関数（coords、item、block）{
coords - クリックが行われたブロックの座標を含むオブジェクト - {x :, y :,
z：} - coords.x、coords.y、coords.z
coords.relative - 潜在的なインストール座標を含むオブジェクト - {x :, y :, z：} -
coords.relative.x、coords.relative.y、coords.relative.z
item - プレーヤーの手札にアイテムを含むオブジェクト - {id :, count :, data：} - item.id、item.count、
item.data
block - クリックが行われたブロック
機能が本体を他の座標に設定した場合
coords.relativeを指定すると、{x :, y :, z：}形式で返されます。
return {x：coords.x、y：coords.y、z：coords.z}
}
Page 4
Block.registerPlaceFunctionForID （ 数値ブロックID、セットアップ関数 ） は完全なアナログです
前のメソッドと同じですが、数値IDを引数として使用します。
Block.setBlockShape （ 数値ブロックID、{x：x 1 、y：y 1 、z：z 1 }、{x：x 2 、y：y 2 、z：z 2 }、data ）
与えられたide上のすべてのブロックに対して、物理的および視覚的な形を与える。ここで、x 1、 y 1 、z 1は、
平行六面体の座標であり、x 2、 y 2 、z 2は有限である。 すべての値は0〜1の範囲です。
それはx 2> x 1、 y 2> y 1、 z 2> z 2である 。
Block.setShape （ 数値ブロックID、x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、data ） は前の方法のアナログです。
Block.getBlockDropViaItem （ block、item、coords ） - 指定した ブロック の推定降下を返します
指定されたオブジェクトによってブロックされます。
Block.setRedstoneTile （ String ID、data、isRedstone ） - ユニットが応答する能力
赤い石の信号、isRedstoneは真、反応は偽、反応しない。
Block.setDestroyTime （ String ID、time ） - ブロック分割の時間を手作業で設定します
秒。
Block.setDestroyLevel （ String ID、level ） - 必要な最小値を設定します。
ブロックの破損を早めるために工具の高さを調整します。
Block.setDestroyLevelForID （ 数値ID、レベル ） は、以前のメソッドのアナログですが、数値のIDを持ちます。
カルベキス
DestroyBlock （ coords、block、player ） - ブロックの破壊。
DestroyBlockStart （ coords、block、player ） - ブロックの破壊の開始点。
DestroyBlockContinue （ coords、block、progress、player ） - ブロックの3回の継続破壊
ダニ。
RedstoneSignal （ coords、params、block ） - redstoneシグナルの変化に反応し、
Block.setRedstoneTile メソッドがブロックに適用されるか、または対応する
パラメータ。 信号強度は0〜15 - params.powerです。
Page 5
モデルブロックを作成する
場合によっては、平行六面体とは形状が異なるブロックを作成する必要があります。
Block.setShapeは役に立ちません。
BlockRenderer.addRenderCallback （ id、function（api、coords、block、_bool） {
}）;
これはブロックレンダラーです。 チャンクのレンダリングを更新するときに呼び出されます。このチャンク内にあります
ブロックのモデルが作成されます。 APIオブジェクトのメソッドはすべて2つのバリエーションに分かれています：メソッドとアナログだけ
ここに割り当てられている後者は同じものをレンダリングしますが、座標は使用しませんが
電流を使用します。
renderBoxId （ x、y、z、x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、id、data ） - 指定されたフォームのボックスを、
データ。
renderBoxIdHere （ x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、id、data ） - 前のメソッドと同様ですが、描画します
coords.x、coords.y、coords.zを調整します。
renderBoxTexture （ x、y、z、x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、name、data ） - 指定されたフォームのボックスを描画します。
ボックスにはこのテクスチャがあります。
renderBoxTextureHere （ x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、name、data ）
coords。
renderBlock （ x、y、z、id、data ） - ブロック全体を描画します。
renderBlockHere （ id、data ） - 同様に、座標からの座標が使用されます。
renderModel （ x、y、z、model ） - 指定された座標にモデルを描画します。
renderModelHere （ model ） - 同様に、座標からの座標が使用されます。
モデル自体について少しはっきりしています。それらはあらかじめ作成されており、メソッドをグループ化することができます
一緒に上記のものが私たちが必要とするものです。
new ICRender.Model （） - ブロックのレンダリングを作成して返します。
BlockRenderer.setStaticICRender （ id、data、render ） - レンダリングを指定するメソッドです。
静的
BlockRenderer.enableCoordMapping （ id、data、model ） - ブロックのレンダリングを動的に変更できます
特定の座標で。
BlockRenderer.mapAtCoords （ x、y、z、render ） - 指定された座標のブロックレンダリングを
属性で指定されたレンダラー、ブロックのメソッド
BlockRenderer.enableCoordMapping 。
BlockRenderer.unmapAtCoords （ x、y、z、render ） - このために標準のレンダリングブロックを置き換えます
ブロックの指定座標のブロックメソッド
BlockRenderer.enableCoordMapping 。
BlockRenderer.createModel （） - 空のモデルを作成して返します。
BlockRenderer.createTexturedBox （ x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、[配列tempus] ） - 作成して返します
ブロックを作成するときと同じフォーマットで指定された、6辺のテクスチャを含むボックスモデル。
Page 6
BlockRenderer.createTexturedBlock （ [テクスチャの配列] ） - ボックスを作成して返します。
ブロックを作成するときと同じ形式で指定された6面のテクスチャを含むフルブロック。
addBox （ x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、id、data ） - ボックスにidを指定してブロックのテクスチャを追加し、
データ。
addBox （ x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、textureName、data ） - テクスチャを含むボックスをモデルに追加します。
addBox （ x 1 、y 1 、z 1 、x 2 、y 2 、z 2 、[テクスチャ配列] ） - モデルにボックスを追加し、テクスチャを指定します
ブロックを作成するときと同じように、配列形式で出力します。
addBox （ id、data ） - モデルに単一のブロックを追加します。
addEntry （ model ） - モデルのレンダラーにブロックを追加します。
テクスチャのアニメーション
インナーコアには、アニメーションブロックを作成するためのツールがあります。例えば、溶岩や
水。 これを行うには、水平方向に16ピクセルのブロックテクスチャを作成する必要があります。
16 *アニメーションのフレーム数、テクスチャはフォームの名前を持つ必要があります
name_name.anim.png。 デフォルトでは、アニメーションはティックで1回変更されます。
これには、number_name.anim.frame.pngあたりのティック数を使用します。
次のページの例
Page 7
1： IDRegistry.genBlockID（ "test_block"）; //一意のパスを作成する
2： var BLOCK_TYPE_TEST = Block.createSpecialType（{
3： 塩基：1、
4： 不透明：真、
5： 爆発：15、
6： 破壊時間：2、
7： redstoneconsumer：真、
8： ライトレベル：0、
9： 色：[0x4444FF]
10： }）;
11： //ブロックの特性を設定する
12： Block.createBlock（ "test_block"、[{name： "テストブロック"、テクスチャ：[["stone"、0]]}]、
BLOCK_TYPE_TEST）; //ブロックを作成する
13： Block.registerDropFunction（ "test_block"、function（coords、id、data、diggingLevel、
toolLevel）{
14： return [[264、Marh.flor（1 + Math.random（）* 8）、0]、[id、1、data]]
15： }）
16： // 1から8までのダイヤモンドとそのブロック自体
17：
18： Block.setDestroyTime（ "test_block"、10）
19： //ブレーク時間を設定する
20： Callback.addCallback（ "DestroyBlockStart"、function（coords、block、player）{
21： if（block.id == BlockID.test_block）{
22： Game.message（ 「 愚か者、あなたは長い間私を壊します 」 ）;
23： }
24： }）;
25： //ブレークポイントの開始時のメッセージ
26： Callback.addCallback（ "DestroyBlock"、function（coords、block、player）{
27： If（block.id == BlockID.test_block）{
28： Game.message（ 「 あなたは私を壊しました... 」 ）;
29： }
30： }）;
31： //ブロックが壊れたときのメッセージ
32： Callback.addCallback（ "RedstoneSignal"、function（coords、params、block）{
33： if（block.id == BlockID.test_block）{
34： Game.message（ 「 赤色のドット信号が変化しましたが、今度は + params.power と同じ です。
35： }
36： }）;
37： // redston信号が変更されたときのメッセージ。
38： var render =新しいICRender.Model（）;
39： BlockRenderer.setStaticICRender（BlockID.test_block、-1、render）;
40： //レンダリングを作成して静的にする
41： var model = BlockRenderer.createTexturedBlock（[[ " stone " 、0]]）;
42： //石のテクスチャでブロックモデルを作成する
43： model.addBox（0.2、1、0.2、0.8、1.2、0.8、 " stone " 、0）;
44： //ブロックの上に石のスラブを作成する
45： render.addEntry（model）
46： //ブロックのレンダリングにモデルをアタッチします。
作成されたSlePe、グループ内のその他のドキュメントhttps://vk.com/modding_inner_core 
