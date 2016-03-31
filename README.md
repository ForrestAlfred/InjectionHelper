# InjectionHelper
Guide To Injection

大家最近都开始用Injection Plugins, 这里给出一些解决方案,
针对在使用过程中遇到的一些问题.


## 1. 真机运行 步骤
大纲:
1. 需要给我们的项目打一个补丁
2. 如果出现 Identity 相关的错误, 需要清理你的证书(普通的清理方法都不彻底, 清理方法后面给出),这里先给出另一个方法,指定 Identity
3. now, enjoy.
实现:
1.在 Project 菜单 找到 Injection Plugin 菜单, 
  在弹出的子菜单里,选择 Patch Project for Injection

2.1. 现在测试一下
  1. 把项目Run 起来
  2. 找个可以主动触发的代码段(Button 的action,TextField的代理 等等,可以回调的地方就行,用来比较注入前后的差别), 在它里面写一句用NSLog ,准备打印一点东西.
  3. 选择 Project 菜单里 Inject Source(快捷键是 ^= )
  4. 如果这时候出现一个进度条一闪而过, 就是注入成功了.(没成功的话会报错)
  5. 再次触发这个代码端, 可以发现我们的NSLog 执行了.

2.2 如果出现Identity 错误,需要指定Identity 的话, 按以下操作执行
