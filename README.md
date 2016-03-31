# Injection 中文指南

大家最近都开始用Injection Plugins, 针对在使用过程中遇到的一些问题, 这里给出解决方案,



## 1. 真机运行步骤

###方法:

1. 需要给我们的项目打一个补丁
2. 如果出现 Identity 相关的错误
  需要清理你的证书(普通的清理方法都不彻底, 清理方法后面给出).这里先给出另一个方法,指定Identity

###实现过程:

1.0 在 Project 菜单 找到 Injection Plugin 菜单, 

  在弹出的子菜单里,选择 Patch Project for Injection
  这会在你的项目目录下生成一个文件夹('iOSInjectionProject')
  
2.1 测试 Injection

  1. Run [Command + R]
  2. 找个可以主动触发的代码段(Button的action 等等,可以回调的地方,用来比较注入前后的差别), 
     在里面加一句 NSLog("Injection Success");
  3. 选择 Project 菜单里 Inject Source(快捷键是 ^= )
  4. 如果这时候出现一个进度条, 一闪而过, 这就是注入成功了.(没成功的话会弹出错误提示框)
  5. 再次触发这个代码端, 可以看到"Injection Success" 被打印了.

2.2 如果在以上过程中出现了错误提示框

  2.2.1 Identity 错误
    
