# Cloud Native Contrail Networking(CN2)概要
CN2は、Kubernetes, OpenShiftで利用可能なCNI(Container Network interface)です。

EVPN/VXLAN, BGP/MPLSをベースとしたアーキテクチャとなり、Kubernetes/OpenShift Cluster内はもちろん、Cluster間接、Cluster外のDataCenterGatewayRouterとの接続やVPN網接続、など柔軟なネットワーク接続を提供します。

CN2特徴

・ハイブリッド・マルチクラウド環境での一貫したネットワーク

・マルチクラスターフェデレーション - 単一のContrail controllerで複数のKubernetes Clusterを管理

・Kubernetes / OpenStack ハイブリッドSDN *future support

・ハイパフォーマンス - DPDK/SmartNIC対応

・GitOpsによるCI/CDパイプライン

# Free Trial
[申請フォーム](https://www.juniper.net/jp/ja/forms/cn2-free-trial.html)

申請後、CN2インストールに必要なhub.juniper.netのアカウントの発行及び、deployer.yamlがダウンロード可能となります。

# Contrail Networking歴史
Juniper Networks社のContrail Networkingは、2012年にContrail Systems社を買収し、リリース以降、パブリッククラウド基盤、プライベートクラウド基盤、キャリアクラウド基盤などさまざまな環境で利用されており、OpenStack分野では最も使われているネットワークプラットフォームとなっています。[OpenContrail Ranked #1 Again!](https://forums.juniper.net/t5/Service-Provider-Transformation/OpenContrail-Ranked-1-Again-Juniper-Brings-Its-A-Game-with-a/ba-p/290851)

2018年にはオープンソースで提供していた「OpenContrail」が、「[Tungsten Fabric](https://tungsten.io/)」と名称を変え、Linux Foundationによってホストされ 、よりニュートラルなオープンソースプロジェクトとなっています。

2019年にはContrail Enterprise Multicloudを発表し、Kubernetes/OpenShift/OpenStackのOverlay接続に加え、DataCenter Fabric(Underlay)も一元管理できるようになりました。

2022年、Contrail NetworkingはCloud Native Contrail Networking(CN2)と名称を変え、Cloud Native環境とより親和性を上げるためにアーキテクチャの変更が行われました。

# チュートリアル
- [CN2 Install](https://github.com/jnpr-jp-crdc/CN2/blob/main/Docs/install.md)
- Namespace
  - Isolated Namespace
  - Pod作成(default-podnetwork)
  - Fabric SNAT
  - Fabric Forwarding
- Virtual Network
  - Network Attachment Definition
  - Pod作成(Contrail Virtual Network)
  - Pod作成(Contrail Multi Virtual Network)
  - Subnet
  - Virtual Network
- Virtual Netowrk Router
  - Mesh Case1
  - Mesh Case2
  - Mesh Case3
  - Hub&Spoke Case1
  - Hub&Spoke Case2
  - Mesh&Hub&Spoke
- Route Leak
  - Same Route Target
  - Router Target Import/Export
- BGPaaS
- VLAN Sub Interface
- Allowed Address Pair (VIP)
- Network Policy
- 外部Router接続
  - Fabric Forwarding
  - Virtual Network
- ClusterIP
- NodePort
- Load Balancer
- Ingress
- KubeVirt
- DPDK
- Port base Mirroring
- Contrail Status
- Analytics
- Lens Extention
- Contrail Pipeline
- Multi-Cluster
