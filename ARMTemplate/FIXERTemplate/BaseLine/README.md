# ARMTemplate - BaseLine

## 概要

- 以下の Azure ポリシーとリソースグループをデプロイする
  - Azure ポリシー
    - Azure リソースをデプロイするリージョンを制限する Azure ポリシー
    - 指定したテナント ID の Azure テナントにのみ、Azure Lighthouse の権限委任を許可する Azure ポリシー
  - リソースグループ
    - Azure DNS を配置するリソースグループ
    - Virtual WAN、Virtual WAN ハブを配置するリソースグループ
    - Azure Bastion Host、仮想ネットワーク、サブネット、パブリック IP、ネットワークセキュリティグループを配置するリソースグループ

## 構成図

![BaseLine 構成図](./BaseLine.png)

## デプロイ方法

1. 以下の[Deploy to Azure]ボタンを押下
2. 以下の各パラメータを指定
   - `サブスクリプション`：リソースのデプロイ先のサブスクリプションを指定
   - `List Of Allowed Locations Parameter`：リソースのデプロイ先として許可する Azure リージョンを指定
   - `List Of Allowed Tenants Parameter`：Lighthouse の権限委任を許可する Azure テナントのテナント ID を指定
   - `Resource Group Location`：リソースグループのデプロイ先のリージョンを指定(東日本:japaneast)
3. 内容に問題がなければ、[確認と作成]からデプロイを実行
 
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ffixer-github%2FFIXER.CloudConfigCMP%2Fdevelop%2FARMTemplate%2FFIXERTemplate%2FBaseLine%2FPolicy_ResourceGroup_template.json)