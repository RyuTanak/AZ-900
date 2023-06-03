# AZ-900の勉強  

学習したことをアウトプットしていく  

# Azureの管理とガバナンスに関する問題  

## Azure AD Identity Protection  
    Azureへのアクセスの際に、セキュリティを高める機能  
    ユーザーのアクセスに様々なポリシーを設定できる  

    〇ユーザーリスクポリシー  
      例えば、リスクが「高」のユーザーをブロックするとか  
      アクセス時にパスワードの変更を求めるとかを設定できる  
    〇サインインリスクポリシー  
      ユーザーリスクポリシーと似ているが、アクセス許可の際にMFAを要求できる  
    〇MFA登録ポリシー  
      特定のユーザー・グループに対して、MFAを強制できる  
    
    また、以下のような機能もある  
    〇レポート  
      全体的なリスクのレポートを出力できる  

【参考】https://qiita.com/zukakosan/items/c95aa55e4263f590b8f6  

## Azure AD Connect Health  
    オンプレミス環境をクラウド上で監視・分析するときに使う機能  
    〇Azure AD Connect  
      オンプレミスのADどAzure ADを同期させる機能  
      オンプレミス・クラウドでアカウントを共有することができたりする  

## Azure ADの特権ID管理(PIM：Privileged Identity Management)  
    ロールを設定する機能。  
    設定時に期限を決めることができるので、プロジェクトの参加期間だけみたいなこともできる  
    → just in time access  

## Azure Advanced Threat Protection(ATP)  
**現在では「Azure Defender for Identity」という名前に変更された**  

    外部からのドメインに対する攻撃を監視するサービス  

【参考】https://juncleit.com/?p=432  

## Azure Defender for Cloud  
    2021年に「Azure Security Center」と「Azure Defender」が名称を変更して「Azure Defender for Cloud」となった  

    クラウドを利用するにあたって、これまでのオンプレミス環境のセキュリティ対策に加えて
    以下の3つの観点が必要になった。  
    1 構成ミスの特定  
    2 形態の違うシステムの保護  
    3 IDの保護  

    これらの実現のために注目されているのが以下の二つ  
    〇Cloud Security Posture Management（GSPM）  
    　→クラウドの設定ミスを防止  
    〇Cloud Workload Protection Platform（CWPP）  
    　→複数のクラウドサービスを一元的に監視・保護  

    Azure Defender for CloudはAzure上でGSPMとCWPPを提供するサービスのこと  

【参考】https://cloud.nissho-ele.co.jp/blog/defender-for-cloud/  

## Azure Policyについて  
    
**Azure Policyは適用前の構成には影響を与えない**  

    リソースグループに仮想ネットワーク（VNet）があります。  
    リソースグループに対して仮想ネットワークの作成・更新が許可されないポリシーを当てても  
    VNetはそのまま機能し続けます。  

## リソースのロック機能  
    サブスクリプション、リソースグループ、リソースの単位で以下のロックレベルを付与できる。  
    〇削除ロック  
    　削除が出来なくなる。読み取りと変更は可能  
    〇読み取り専用ロック  
    　読み取りだけできる。削除と更新が出来なくなる  
    
    複数ロックも可能  

## サポートリクエスト  
    ポータル画面から、ヘルプとサポート機能でサポートリクエストを行うことができる。  
    また、Azure サポートチケット REST APIを使ってもサポートリクエストを送ることができる  

## Knowledge Center  
    ※もしかして古い名前？Resource Centerという名前かも  

    Azureに関する一般的な質問とその回答をまとめたもの  

## Azure 料金計算ツール  
    https://azure.microsoft.com/ja-jp/pricing/calculator/  
    上記のサイトで、例えば、VMの使うことを仮定し設定項目を入れていったら、その利用料金が分かる  
    個別のサービスを利用した際の詳細な見積もりに使用  

## Azure TCO 計算ツール  
    Azureを利用した総コストを見積もるツール  
    https://azure.microsoft.com/ja-jp/pricing/tco/calculator/  

## Azure Advisor  
    VMの実行コストを削減するなどの推奨事項を提供する  
    コストを最適化するために使用できるツール  

## Azure Reservations　　
    Reservations：予約  
    Azureのサービスに割引料金を提供するサービス  

## パブリックプレビュー  
    全てのユーザーが利用できる、試験利用期間のこと。  

## Powershell  
    Windows、Linux、macOSにインストール可能  

## 仮想マシンのステータス  
    〇停止（割り当て解除）  
    　シャットダウンを開始すると、実行中→停止となる  
    　停止したら、課金はされない。  
    〇停止済  
    　リソースがまだ割り当てられているので、課金は発生する  

## Azure ADに参加できるデバイス  
    〇Windows10  
    〇Windows11  
    ちなみに、Homeエディションは対象外  
    