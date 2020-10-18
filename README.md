# wechat-zabbix-message
#前提调用条件，申请微信公众号或者app小程序之类的
#配置脚本里的CorpID是企业号的标识， Secret是管理组凭证密钥，应用ID 


    User = sys.argv[1]                                                                # zabbix传过来的第一个参数
    Subject = str(sys.argv[2])                                                        # zabbix传过来的第二个参数
    Content = str(sys.argv[3])                                                        # zabbix传过来的第三个参数


    Corpid = "wx7cdasdff51151f"                                                         # CorpID是企业号的标识
    Secret = "ZdaWqasdfafdfgATAgaaFn3ieXQA8o_Xl9ZinBSavqEOGkFZE"                        # Secret是管理组凭证密钥
    #Tagid = "1"                                                                        # 通讯录标签ID
    Agentid = "1000002"                                                                 # 应用ID 
    #Partyid = "1"                                                                      # 部门ID
   

配置好后，将脚本放到zabbix 脚本调用目录


 /etc/zabbix/alertscripts/wechart.py



zabbix调用配置

切换菜单到   报警消息操作
```shell
默认标题： {HOST.NAME} 的{TRIGGER.NAME}警告！！！
消息内容：

故障告警:
主机: {HOST.NAME}
IP:{HOST.IP}
事件发生在： {EVENT.TIME}  {EVENT.DATE}
触发器: {TRIGGER.NAME}
当前状态：{TRIGGER.STATUS}:{ITEM.VALUE1}

事件 ID: {EVENT.ID}
{TRIGGER.URL}




切换菜单到   恢复消息操作
```shell
默认标题：{HOST.NAME} 的{TRIGGER.NAME}恢复提示！

消息内容：
主机: {HOST.NAME}
IP:{HOST.IP}
事件发生在： {EVENT.TIME}  {EVENT.DATE}
触发器: {TRIGGER.NAME}
当前状态：{TRIGGER.STATUS}:{ITEM.VALUE1}

事件 ID: {EVENT.ID}
{TRIGGER.URL}






# yum -y install epel-release
# yum -y install python-pip
# pip install --upgrade pip
# pip install requests





