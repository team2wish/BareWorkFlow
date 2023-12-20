ReactNative Doc
https://reactnative.dev/docs/getting-started
***

1. Wachmanのインストール
[Watchman は](https://facebook.github.io/watchman)、ファイルシステムの変更を監視するための Facebook のツールです。パフォーマンスを向上させるために、インストールすることを強くお勧めします。
```Homebrew
brew install watchman
```

2.  Xcodeインストール

3. 新規プロジェクト作成（Expoを使用しない）
```npm 
npx react-native@latest init <プロジェクト名>
```
3. 新規プロジェクト作成（Expoを使用）
```npm
npx create-expo-app@latest --template tabs@49 .
```

[ExpoWorkflow（Bare or Managed）](https://qiita.com/mildsummer/items/64d902c3a2cc58f1f590)



※ Expoを使用しないバージョンで`npm run ios`が正しく動作しない
実施内容
```npm
brew install rbenv
```

```npm
rbenv install 3.2.2
```

```npm
gem install drb -v 2.0.5

--- エラー内容 ---
Fetching drb-2.0.5.gem
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory.
```
[上記エラー解決法](https://qiita.com/nishina555/items/63ebd4a508a09c481150)

```npm
sudo gem install cocoapods
```

ReactNative Debuggerのインストール
```npm
brew update && brew install --cask react-native-debugger
```

ReactNative キャッシュを削除して再起動
```npm
npx react-native start --reset-cache
```

現在使用しているPORT対象
```npm
lsof -i :<PORT番号>
```


利用可能デバイスの確認
```npm
xcrun simctl list devices
```
デバイス指定
```npm
npx react-native run-ios --simulator="iPhone 15Pro"
```

[下記エラーの解決法](https://stackoverflow.com/questions/57822215/main-jsbundle-file-showing-in-my-ios-project-but-still-throwing-no-bundle-url-p)
[パート２](https://qiita.com/nekoniki/items/c466997026883fb547ea)

1. main.jsbundleファイルの作成
```npm
npx react-native bundle --platform ios --dev false --entry-file index.js --bundle-output ios/main.jsbundle
```

2. Xcodeでmain.jsbundleファイルを読み込む
```npm
open <SecondVoice(ファイル名)>.xcworkspace
```

↓Xcode画面
main.jsbundleファイルはドラック&ドロップで追加
![[スクリーンショット 2023-12-20 1.24.33.png]]

![[スクリーンショット 2023-12-20 0.07.13.png]]
