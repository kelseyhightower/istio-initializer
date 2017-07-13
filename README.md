# Istio Initializer


## Usage

Create the Istio Initializer `initializer-config`:

```
kubectl apply -f initializer-config.yaml
```

Create the Istio Initializer `configmap`:

```
kubectl apply -f configmaps/istio-initializer.yaml
```

Process uninitialized pods:

```
istio-initializer --kubeconfig ~/kubeadm-single-node-cluster.conf
```
``` 
2017/07/13 06:01:39 Starting the istio initializer...
2017/07/13 06:01:39 Initializer name set to: initializer.istio.io
2017/07/13 06:01:59 initializing pod: nginx-2092552835-6zmds
```

> This is currently a noop, which just removes the istio initializer from the list of pending initializers
