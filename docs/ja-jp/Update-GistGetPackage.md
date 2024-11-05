# Update-GistGetPackage

インストールされているすべてのパッケージを更新します。

GistGetで定義されているものだけでなく、ローカルにインストールされているパッケージすべてが対象です。

```pwsh
Update-GistGetPackage
```

GistGetではパッケージのバージョンを指定することができます。

```yaml
7zip.7zip:
  version: 1.0.0
```

GistGetのバージョン定義と、ローカルにインストールされているバージョンの組み合わせによって動作が変わります。

|ローカルバージョン|動作|
|--|--|
|＝1.0.0|新しいバージョンがリリースされていても更新されません。|
|≠1.0.0|1.0.0に置き換えるか確認の上、1.0.0に置き換えます。|
|未インストール|インストールされません。インストールするにはSync-GistGetPackageを利用します。|

# Parameters

なし