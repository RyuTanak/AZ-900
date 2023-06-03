# AZ-900の勉強  

学習したことをアウトプットしていく  

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

