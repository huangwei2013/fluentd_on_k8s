# fluentd_on_k8s
kubernetes环境中使用efk的方法

## 文档说明

### es安装
包括：
* es单节点docker安装方式
* elasticsearch-head 工具安装方式

### fluentd安装和配置
fluentd在K8S上安装用yaml文件，按执行顺序如下：
* fluentd-es-services.yaml：账号等
* fluentd-es-configmap.yaml：fluentd的配置内容
* fluentd-es-ds.yaml：fluentd的k8s deployment内容，其中至少 FLUENT_ELASTICSEARCH_HOST 需要按照你的环境配置

### [TODO] Java 通过 es api 访问示例代码


## 效果说明
#### fluentd
* 索引
支持按照K8S中，不同namespace和应用名称，按天建立索引。

如索引名称为：
```
kubes_kube-system.kuboard-2020.09.21
```



## 相关资源

* [fluentd官网文档](https://docs.fluentd.org/)
* [fluentd代码](https://github.com/fluent/)
* [kuboard，再常用不过的k8s管理界面](https://www.kuboard.cn/)
