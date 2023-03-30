# VOICEVOX CORE Go サンプル

音声合成ライブラリ[VOICEVOX CORE](https://github.com/VOICEVOX/voicevox_core)を Go から使用するサンプルコード (`main.go`) です。詳細はそちらをご覧ください。

ビルドするために Go の開発環境が必要です。

## Windows の場合

(現在、Windows のみの対応となっております)

### 必要なファイルの準備

voicevox_core のダウンローダーを任意のディレクトリで実行してください。

(ダウンローダーの説明:https://github.com/VOICEVOX/voicevox_core/blob/main/docs/downloads/download.md)

生成されたフォルダ(voicevox_core)内のファイル・フォルダのうち、以下を`windows/`に配置してください。

```
model
open_jtalk_dic_utf_8-1.11
onnxruntime.dll
voicevox_core.dll
```

### ビルド&実行

`windows/`に移動します

```
cd windows
```

以下のコマンドを実行すると、`simple_tts.exe`が作成、実行されます:

```shell
go build
./simple_tts
```

正常に実行されれば `speech.wav` が生成されます。以下のコマンドで再生することができます：

```shell
$player = New-Object Media.SoundPlayer "./speech.wav"
$player.Play()
```

## Mac/Linux

現在、本サンプルは Windows のみの対応となっています。

ソースコードを見ての通り実態は`.dll`ファイルを呼び出しているだけのため、`.so`に読み替えれば実行できるかと思いますが、検証ができていないため、非対応とさせていただいております。

Mac/Linux での検証をしてくださった場合はぜひ PR などでお知らせください。

## ライセンス

ソースコードのライセンスは[VOICEVOX CORE](https://github.com/VOICEVOX/voicevox_core)と同じ [MIT LICENSE](./LICENSE) です。

ただし、本サンプル実行時に使用する VOICEVOX CORE のビルド済みライブラリは別ライセンスのため、ご注意ください。
