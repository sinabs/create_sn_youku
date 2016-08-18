= 生成优酷路由宝sn序列号 =
此程序修改eeprom.bin的mac生成新sn序列号,可以解决无法解绑路由器
生成新sn序列号重新绑定,此脚本仅供学习研究

== 依赖环境
php-cli
php-gmp扩展

== 操作步骤
1. 路由器断电,按住rest键进入`Breed Web 恢复控制台` > `固件备份` > 下载`EEPROM`
2.备份下eeprom.bin,然后执行

    ./create_sn_youku  eeprom.bin
    offset:8 12 => 13
    offset:9 8c => 8d
    offset:44 1f => 20
    offset:45 66 => 67
    offset:50 1f => 10
    offset:51 67 => 78
    mac:A061B2FD1078 sn:2115665387814145
    
3.`Breed Web 恢复控制台` > `固件更新` > `EEPROM` 选择修改后的eeprom.bin
4.然后在`Breed Web 恢复控制台` > `固件更新` > `固件` 选择优酷路由宝官方固件(我用2.1.0613.8617版本)

测试设备是`OYE路由器`,验证可以成功洗白