## kubernetesクラスタとkubectlのバージョン確認
```
kubectl version
```

## Context一覧を取得する
```
kubectl config get-contexts
```

## Context の切替
```
kubectl config use-context <Context名>
```

## 利用可能なリソース種別の一覧取得
```
# すべてのリソース種別を表示
kubectl api-resources

# Namespaceに属しているリソース
kubectl api-resources --namespaced=true

# Namespaceに属していないリソース
kubectl api-resources --namespaced=false
```
## すべてのリソース一覧を取得
```
kubectl get $(kubectl api-resources --namespaced=true --verbs=list -o name |tr '\n' ',' |sed -e 's|,$||g')
```
