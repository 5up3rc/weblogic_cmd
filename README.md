# weblogic_cmd
weblogic t3 deserialization rce

1. 直接通过加载字节码的方式来加载class，执行无文件生成。通过绑定rmi来实现回显。
2. 支持t3s
3. 支持StreamMessageImpl,MarshalledObject绕过

使用说明：
  -H 远程目标主机
  -P 远程目标端口
  -C 需要执行的命令
  -T 可选的绕过方式
  -U 删除绑定的rmi实例
  -B 通过payload直接调用系统命令－针对没法回显的情况下使用
  -os 指定目标操作系统
  -https 使用tls的指定
  -shell 以shell的方式展现
  -upload 上传文件 需要配合-src -dst
  -src 需要上传的文件路径
  -dst 需要上传文件至目标的路径
  -noExecPath 在某些没有/bin/bash 或者cmd.exe情况下使用
