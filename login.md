> Client e = new Client();
> String result = e.uc\_user\_login("username", "password");

> LinkedList[String> rs = XMLHelper.uc\_unserialize(result);
> if(rs.size()>0){
> > int $uid = Integer.parseInt(rs.get(0));
> > String $username = rs.get(1);
> > String $password = rs.get(2);
> > String $email = rs.get(3);
> > if($uid > 0) {
> > > System.out.println("登录成功");
> > > System.out.println($username);
> > > System.out.println($password);
> > > System.out.println($email);


> String $ucsynlogin = e.uc\_user\_synlogin($uid);
> System.out.println("登录成功"+$ucsynlogin);

> //本地登陆代码
> //TODO ... ....
> } else if($uid == -1) {
> > System.out.println("用户不存在,或者被删除");

> } else if($uid == -2) {
> > System.out.println("密码错");

> } else {
> > System.out.println("未定义");

> }
> }else{
> > System.out.println("Login failed");
> > System.out.println(result);

> }