# Introduction #

同步登陆实现方法介绍

# Details #

现找到UC.java

里面有一个方法
```
protected String doAnswer(HttpServletRequest request, HttpServletResponse response){
     //处理
     String $code = request.getParameter("code");
     if($code==null) return API_RETURN_FAILED;

     //....
}

```
所有同步操作在此方法中实现。

你可以根据同步的“代码”设定执行方法来实现你的功能。（这部分工作必须由你来实现）

```
		} else if($action.equals("synlogin")) {

			if(!API_SYNLOGIN ) return (API_RETURN_FORBIDDEN);

			doLogin(request, response, $get);


		} else if($action.equals("synlogout")) {

			if(!API_SYNLOGOUT ) return (API_RETURN_FORBIDDEN);

			doLogout(request, response, $get);
}

//添加如下方法：并实现他
	
    protected void doLogin(HttpServletRequest request, HttpServletResponse response,Map<String,String> $get){
    
	}
    protected void doLogout(HttpServletRequest request, HttpServletResponse response,Map<String,String> $get){
        
	}
    protected void doUpdatePwd(HttpServletRequest request, HttpServletResponse response,Map<String,String> $get){
        
	}
```