# F.O.X SDK の削除確認方法
<div id="delete_unity"></div>

# Unity

## ライブラリの削除

以下のF.O.XのSDKに含まれるファイルがある場合は削除してください。

[F.O.X Unity SDK 4.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/4.x/lang/ja/doc/integration/README.md)

[F.O.X Unity SDK 3.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/3.x/lang/ja/doc/integration/README.md)

### iOSの場合

以下のファイルがある場合は削除してください。

- `CYZFox.framework`
- `libFoxSdk.a` 
- `AdManager.h`
- `Ltv.h`
- `AnalyticsManager.h`

F.O.Xにて追加したフレームワークで他で利用していないものを削除してください

[フレームワーク設定 4.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/4.x/lang/ja/doc/integration/ios/README.md)

[フレームワーク設定 3.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/3.x/lang/ja/doc/integration/ios/README.md)

### Androidの場合

`build.gradle`に以下の設定がある場合は削除してください。

#### F.O.X 4.X

```gradle
repositories {
    maven {
        url "https://github.com/forceoperationx/public-fox-android-sdk/raw/master/mavenRepo"
    }
}

dependencies {
    implementation 'co.cyberz.fox:track-core:{VERSION}'
}
```

```gradle
dependencies {
	implementation files('libs/foxtrack-core_{VERSION}.jar')
}
```

#### F.O.X 3.X

```gradle
repositories {
    maven {
        url "https://github.com/cyber-z/public-fox-android-sdk/raw/master/mavenRepo"
    }
}

dependencies {
    compile 'co.jp.cyberz.fox:sdk-android:X.X.X'
}
```

以下で追加した設定で不要なものを削除してください。

[Android プロジェクトの詳細設定 4.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/4.x/lang/ja/doc/integration/android/README.md)

[Androidプロジェクトの設定 3.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/3.x/lang/ja/doc/integration/android/README.md)


## インストールリファラの削除

manifest.xmlの以下の設定を削除してください。

[インストールリファラ計測の設定 4.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/4.x/lang/ja/doc/integration/android/README.md#fox-unity-sdk-415%E3%81%BE%E3%81%A7%E3%81%AE%E5%8F%A4%E3%81%84%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B3%E3%81%AE%E5%A0%B4%E5%90%885)

[インストールリファラ計測の設定 3.X](https://github.com/forceoperationx/public-fox-unity-sdk/blob/3.x/lang/ja/doc/integration/android/README.md#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%83%AA%E3%83%95%E3%82%A1%E3%83%A9%E8%A8%88%E6%B8%AC%E3%81%AE%E8%A8%AD%E5%AE%9A)

## コード/その他ファイル全体

F.O.Xでの計測のために追加したコードを削除してください。

また、コード/ファイル全体を対象に、以下の単語を検索し、含まれてる場合は適宜削除してください。
大文字小文字の区別なしで検索してください。

- `FOX`
- `F.O.X`
- `forceoperationx`
- `app-adforce`
- `appadforce`
- `cyberz`
- `cyber-z`
- `cyz`

