> Client uc = new Client();

> //setcookie('Example\_auth', '', -86400);
//		生成同步退出的代码
> String $ucsynlogout = uc.uc\_user\_synlogout();
> System.out.println("退出成功"+$ucsynlogout);