#Windows

参考
https://zhuanlan.zhihu.com/p/29581818

交换步骤：
1. 打开Windows注册表编辑器（在cmd或powershell命令行下键入regedit回车即可打开）
2. 在"HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout"这个项下新建一个名为"ScanCode Map"键（右键新建二进制值）
3. 右键名称列下的这个"ScanCode Map"修改，依次键入编辑"hex:00,00,00,00,00,00,00,00,03,00,00,00,30,00,1e,00,1e,00,30,00,00,00,00,00"
4. 修改完了后并不能立即生效，因为是通过注册表修改底层键位映射所以需要重启计算机，重启资源管理器也是没有用的

还原有2种方法：
1. 从注册表中删除你创建的ScanCode Map这个键
2. 用"hex:00,00,00,00,00,00,00,00,01,00,00,00,00,00,00,00"覆盖掉原来的值