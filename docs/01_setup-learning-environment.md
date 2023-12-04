# パート１ : ハンズオン環境の構築

azure-cliとbicepというツールを使って、ハンズオン環境を構築します。

## 事前準備

* Azureサブスクリプション
* Azure CLI
* bicep
* .NET 7.0 SDK
* Entity Framework Coreツール

## az ログイン

az loginを実行して、Azureにログインします。

```bash
az login
```

サブスクリプションが複数ある場合は、以下のコマンドで確認できます。

```bash
az account list --output table
```

ログインしたいサブスクリプションのIDをコピーして、以下のコマンドを実行します。

```bash
az account set --subscription <サブスクリプションID>
```

## bicepのインストール

bicepをインストールします。

```bash
az bicep install
```

bicepがインストールされたことを確認します。

```bash
az bicep --help
```

## .NET7のインストール

[公式ページ](https://dotnet.microsoft.com/ja-jp/download/dotnet/7.0)からdotnetをインストールします。

インストールが完了したら、以下のコマンドを実行して、dotnetがインストールされたことを確認します。

```bash
dotnet --version
```

## Entity Framework Core ツールのインストール

以下のコマンドを実行して、Entity Framework Coreツールをインストールします。

```bash
dotnet tool install --global dotnet-ef
```

インストールが完了したら、以下のコマンドを実行して、Entity Framework Coreツールがインストールされたことを確認します。

```bash
dotnet ef --version
```

## リポジトリのクローン

このリポジトリをクローンします。

```bash
git clone
```

## ディレクトリの移動

クローンしたリポジトリのディレクトリに移動します。

```bash
cd azure-hands-on
```

## スクリプトの実行

以下のコマンドを実行して、ハンズオン環境を構築します。

### Windowsの場合

```bash
./scripts/resource-deploy.ps1
```

### Macの場合

```bash
source ./scripts/resource-deploy.sh
```

`Are you sure you want to execute the deployment? (y/n):` と聞かれたら、`y`を入力してEnterを押します。


## リソースの確認

デプロイが完了したら、Azureポータルを開きます。
`rg-azureops-sampleapp`リソースグループを開きがリソースが作成されていることを確認します。

ここにイメージを入れる

NEXT ＞ [パート２ : シークレットをセキュアに管理する](./02_securely-managing-secrets-with-key-vault.md)  
TOP  ＞ [トップページに戻る](/README.md)