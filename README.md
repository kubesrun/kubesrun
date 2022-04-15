# kubesrun
## 项目目标
降低 Kubernetes 的使用门槛，让开发和测试也能很轻松地进行发布工作。精细化管理各类权限，例如特定的人只能看到和操作特定的应用；固定应用只能挂载指定的 Secret 和 ConfigMap，ConfigMap 指定内容隐藏；发布操作开启审批、配置审批流程等。
## 用户群体
需要进行 CICD 的用户，可以是运维、开发、测试等人员。
## 流程图
### 普通发布全流程（不代表最终流程）
![image](https://user-images.githubusercontent.com/38366752/163560148-a65fa706-a79d-4686-a765-e2285aa88aee.png)

### 新建应用流程（不代表最终流程）
![image](https://user-images.githubusercontent.com/38366752/163560252-90840245-f923-4e21-937c-f4e87c29f337.png)

### 发布应用用户流程图（不代表最终流程）
![image](https://user-images.githubusercontent.com/38366752/163560273-9e3fce52-102b-4611-bf4a-7d89d69035a3.png)

## 依赖的服务
git 仓库
镜像仓库
Kubernetes 集群
## 主要功能点
对 deployment、job 等类型资源的一般发布、回滚支持，即发布只需要填写容器信息。
service、ingress 的可视化配置和yaml直接编辑，支持主流 ingress 
ci 能力
发布过程、状态可视化
操作记录可追溯
容器日志查看
多应用发布编排
多环境发布编排
灰度发布、蓝绿发布能力
其它 k8s 资源增删查改操作能力
对发布人员的权限控制，指定的人只能进行执行特定的操作，例如A用户只能发布a-app应用，A用户无法查看b-app的状态及相关日志。引申至其他各类K8S资源。
一键部署脚本
配置单独作为一个模块
灰度发布的实时流量比例显示
