# Introduction #

刚注册用户第一访问其它应用的时候需要在该App重新login一次。

# 主要原因 #

以Ucenter为基础的app的会员信息是相互独立，只有会员帐号是共享的，刚注册的用户只保存在当前APP和Ucenter中。然而，UCenter的下的App会在登陆的时候去同步Ucenter的会员系统。如果当前App没有当前帐号，则会将该用户资料添加该子App系统中去。