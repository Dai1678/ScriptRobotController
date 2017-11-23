# ScriptRobotController
スクリプト組み立て型 ロボPArduinoラジコンシステム (操作コントローラー用Androidアプリ) 

ラジコン側のプログラム : https://github.com/Dai1678/ScriptArduinoRC   

# 目的
GUIでプログラムのフローチャートを作って、ラジコンを動かす　⇛　思い通りの動作を実行させるための論理的思考力を養おう   

# 開発環境
AndroidStudio 3.0.1 (gradle3.0.1)
java

# 動作確認環境
デバッグできた端末を追記

# 開発中で使用する用語
- イメージ(image)　 ：　前進や後退などのラジコン各処理のこと
- スクリプト(script)：　複数のイメージを組み合わせて、上から順に実行させるかたまり
- イメージエリア(imageList)　：　イメージが置いてある領域 ボタンを押すorここからドラッグしてスクリプトを追加する
- スクリプトリスト(scriptList) : 実行させるイメージが置いてある領域 上から順に実行させる

# 実装内容   
## A実装
- イメージエリア、スクリプトリストの作成
- イメージをButtonで表示し、スクリプトに追加できるようにする
- スクリプトリストにある各イメージの削除
- 各イメージの実行秒数の設定
- スクリプトをArduinoにBluetoothで送信 (送信ボタン実装)

## B実装
- イメージをドラッグでスクリプトに追加できるようにする
- スクリプトに追加した各イメージの並び替え
- アプリ側でモータ値の設定
- アプリレイアウトの確定

## C実装   
- スクリプト送信ボタン実行後にスクリプト実行ボタンに変化させて、そのままラジコンを走らせる   

# 扱うデータ
- 各イメージ　(前進(0001)、後退(0002)、左回転(0003)、右回転(0004)、停止(0005))
- イメージの実行時間[s] (0002 : 2秒) 
- モータパワー値  ラジコンモータをどの程度のチカラで回すか　(0〜255) ※電池残量にとても左右される
