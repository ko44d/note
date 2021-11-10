## Kubernetesオブジェクト
- Kubernetes上で永続的なエンティティである
- Kubernetesはこのエンティティを使い、クラスターを表現する
- Kubernetesは意図の記録である
- 一度Kubernetesオブジェクトを作成すると常にそのKubernetesオブジェクトが存在し続けるように動く

## Kubernetesオブジェクトのspec（仕様）/status（状態）
- Kubernetesオブジェクトを管理する2つの入れ子になったオブジェクトフィールドを持つ
- specオブジェクトとstatusオブジェクトである
- specオブジェクトとは、オブジェクトの望ましい状態を記述する。オブジェクトに持たせたい特徴を表現する
- statusオブジェクトとは、オブジェクトの現在の状態を示す。この情報はKubernetesから与えられ、更新される

## Deploymentとは
- ユーザが理想的な状態を定義する。指定された頻度で現在の状態を理想的な状態に変更する
- コンテナの実行状況を継続的にチェックする。終了していることを検出した場合に即座に再起動するプログラムである

## Podとは
- 一つ以上のコンテナのグループを表現するKubernetesオブジェクトである
- クジラの小規模な群れを意味する用語である

## ReplicaSetとは
- 同一のPod（レプリカグループ）を管理することである
- DeploymentがPodを直接管理するのではなく、ReplicaSetが行う

## 参考
- [Kubernetesオブジェクトを理解する](https://kubernetes.io/ja/docs/concepts/overview/working-with-objects/kubernetes-objects/)
