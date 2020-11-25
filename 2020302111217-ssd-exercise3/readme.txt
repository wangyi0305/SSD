一.源文件read:
1.CatFish.java文件声明了Catfish类，
  两个属性column和energyLevel,即为列和精力等级。
   三个方法 :  getColumn(获取column的值)： 返回值为column
	    swinRight（往右游）：即为了实现点一下向右游一格，用函数则为每次column+1，eL-1（column在10以内）
  			       若column大于10，则设置其值为10（鱼不动）
	    getImage(获取图片)：返回eL对应的鱼的图标
2.HtmlImage.Java文件声明了HtmlImage类
   声明两个字符串：imageName（图片名称）
    	              alternateText(如果图像不可用,要显示的文本)
   构造一个带两个参数的方法：HtmlImage,其中两个参数分别是前面两个字符串的值
   声明一个可变字符串，为了后面显示图片
3.HtmlTable.java
   大概是在构造池塘的格子（即表格）。
4.HtmlAnchor.java
    声明HtmlAnchor 类 允许编程访问服务器上的 HTML <a> 元素(就是建立超链接)
5.HtmlPage.java		
     声明HtmlPage类，便于Servlet new出来它从而创建新的页面	
6.Simulation.java
    声明Simulation类，初始化一个模拟池塘
7.SimulationServlet.java
    第一次跳转到的servlet，即用来create a catfish
8.SimulatinView.java
    第二次跳转到的servlet，主要的实验显示由它来完成
我修改的源文件：
1.配置index.html表单里的method="POST",action="/catfish/SimulationServlet"
  （这里我只能采用较长的 url，否则找不到）	
2.修改catfish.java:写入getCloumn方法的语句是return colum;用if else 结构写swimRight方法，实现鱼的游动和精力递减
   用if else结构写getImage，实现catfish在不同energy level时的图片（这里配置了两张不同catfish图片的url）
3.修改SimulationView.Java：分别配置了向右箭头图片和空白图片的url。 

