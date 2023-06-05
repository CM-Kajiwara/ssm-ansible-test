# 

## Ansibleでの管理対象

SecureAgentの構築後の共通で入れるミドルウェアの導入を定義しています。

## 追加方法

ミドルウェア単位で `roles/REL8` に必要なファイルを追加します。

jqのインストールだとこんな感じのファイルを作成することでパッケージマネージャからの取得を行ってくれます。

### roles/REL8/system/jq/tasks/main.yml

```
- name: install jq
  yum:
    name: jq
    state: present
    update_cache: yes
```