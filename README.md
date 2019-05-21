## Playground stuff for [tgik.io/075](https://tgik.io/075)

to use this stuff check out the link above.

```terminal
git clone https://github.com/mauilion/kind-cni-playground
cd kind-cni-playground/flannel
ln -sfn $(pwd)/cni /tmp/cni
cat config
kind delete cluster
kind create cluster --config config
export KUBECONFIG="$(kind get kubeconfig-path --name="kind")"
k cluster-info
kubectl get --all-namespaces -o
kubectl get --all-namespaces -o wide
kubectl get nodes --all-namespaces -o wide
kubectl get pods --all-namespaces -o wide
kubectl get pods -o wide
```