# 课工场Java学习

## 第一节	While循环

| **快捷键** |                                                         |
| ---------- | ------------------------------------------------------- |
|            | alt + /                    提示                         |
|            | ctrl + shift + O     导包                               |
| **语法**   |                                                         |
|            | while(条件){                                            |
|            | 内容                                                    |
|            | }                                                       |
|            | 步骤：1.变量初始化，2条件判断，3执行循环内容，4变量迭代 |
|            | 顺序：1，2，3，4，  2，3，4，，，，，，， 2   结束      |

| 单词 | public | 公有的 |
| ---- | :----- | :----- |
|      | static | 静态的 |
|      | void   | 空     |
|      | main   | 主要的 |
|      | String | 字符串 |
|      | System | 系统   |
|      | out    | 输出   |
|      | print  | 打印   |
|      | result | 结果   |
|      | count  | 计数   |

### 1、设置自定义变量：**

```java
public class While {
	public static void main(String[] args) {
		int count=0;
		while(count<50){
			System.out.println("做"+(count+1)+"俯卧撑");
			count++;
		}
	}
}
```

### **2、设置手动在控制台输入判断条件：**

```java
public static void main(String[] args) {
	Scanner scanner=new Scanner(System.in);
	String result="n";
	while (result.equals("n")) {
		System.out.println("做俯卧撑");
		System.out.println("高兴了吗？（y/n）");
		result=scanner.next();	
	}
}
```
### **3、求100的累加和：**

```java
public static void main(String[] args) {
	int i=1;
	int sum=0;
	while (i<=100) {
		sum+=i;
		i++;		
	}
	System.out.println("总和："+sum);
}
```

### 4、作业：

```java
package wile;
//1.求和：1到100之间【不能被3整除】的数字的和？
public class Homework1 {
    public static void main(String[] args) {
    	int i=1;
    	int sum=0;
    	while (i<=100) {
			if(i%3!=0){
				sum+=i;
			}
			i++;
		}
    	System.out.println(sum);
}
}
```

```java
package wile;
//2.鸡兔同笼：在一个笼子里，有35只鸡和兔子，共有94条腿，求出一共有几只鸡，几只兔子？
public class Homework2 {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int y=1;
		//共有动物35只，脚94只；
		//x+y=35，2x+4y=94
		//x=35-y;
		//2(35-y)+4y=94
		//2y=24
		//y=12
		while (y<94/4) {
			
			int x=35-y;
			if (2*x+4*y==94) {
				System.out.println("鸡有："+x+"只，"+"兔有："+y+"只，");
			}
			y++;
		}

	}

}
```

**逢7过：**

```java
public static void main(String[] args) {
	int sum=1;
	while (sum<=100) {
		if (sum%7==0) {                    //去除7的倍数
			System.out.println("过");
		}else if (sum%10==7) {             //去除个位上是7的数
			System.out.println("过");
		}else if (sum/10==7) {             //去除十位上是7的数
			System.out.println("过");
		}
		else {
			System.out.println(sum);
		}
		sum++;
	}
}
```
## 第二节	for循环

| 语法 |                                                 |
| ---- | ----------------------------------------------- |
|      | for(1变量初始化; 2条件判断; 4变量迭代){         |
|      |                                                 |
|      | }                                               |
|      | 顺序：1，2，3，4，2，3，4，2，3，4，，，，，，2 |

| 循环总结 |           |                      |                    |
| -------- | --------- | -------------------- | ------------------ |
|          | while循环 | 不确定循环次数的场合 |                    |
|          | for循环   |                      | 确定循环次数的场合 |

| 随机数 |               |                                                     |
| ------ | ------------- | --------------------------------------------------- |
|        | Math.random() | 生成一个0-1之间的随机数，最小值为0，最大值无限接近1 |

| 控制台输入步骤 |            |                                          |                        |
| -------------- | ---------- | ---------------------------------------- | ---------------------- |
|                | 1.创建对象 | Scanner input = new  Scanner(System.in); |                        |
|                | 2.导入包   | ctrl + shift + O                         |                        |
|                | 3.调用方法 | input.next();                            | 从控制台获取一个字符串 |
|                |            | input.nextInt();                         | 从控制台获取一个整数   |
|                |            | input.nextDouble();                      | 从控制台获取一个小数   |

| 单词 | Scanner | 扫描仪 |
| ---- | ------- | ------ |
|      | integer | 整数   |
|      | double  | 双     |
|      | next    | 下一个 |
|      | Math    | 数学   |
|      | if      | 如果   |
|      | else    | 其他的 |

### 1.求和：1到100之间【不能被3整除】的数字的和？

```java
public static void main(String[] args) {
		int sum=0;
		for (int i = 1; i <= 100; i++) {
			if (i%3!=0) {
				sum+=i;
			}
		}
		System.out.println(sum);
	}
```

### 2.鸡兔同笼：在一个笼子里，有35只鸡和兔子，共有94条腿，求出一共有几只鸡，几只兔子？

```java
public static void main(String[] args) {
		int ji;
		for (ji = 0; ji <35 ; ji++) {
			if (2*ji+4*(35-ji)==94) {
				System.out.println("鸡有："+ji+"只");
				System.out.println("兔有："+(35-ji)+"只");
			}	
		}
	}
```

### 3.逢7过：

```java
public static void main(String[] args) {
		for (int i = 1; i <= 100; i++) {
			if (i%7==0) {
			System.out.println("过");
			}else if (i%10==7) {
				System.out.println("过");
			}else if (i/10==7) {
				System.out.println("过");
			}
			else {
				System.out.println(i);
			}	
		}
	}
```

### 4.猜数字

随机生成一个1到100之间的随机数
循环猜数字，如果猜测的数字比随机数大的话，提示大了一点，反之提示小了一点
最后统计猜的数字，显示结果，如果一次猜中的话，则提示，你是个大神，2-5次，提示天才，6-7次，提示普通人，8次以上，提示你哦买噶的，你太艰辛了！。

```java
public static void main(String[] args) {
	Scanner input=new Scanner(System.in);
	int suijishu=(int)(Math.random()*100+1);
	int num=0;
	int count=0;
	System.out.println("我心里有个数字（1-100），你来猜一下喽？");
	while (num!=suijishu) {
		count++;
		num=input.nextInt();
		if (suijishu>num) {
			System.out.println("你猜的小了一点");
		}else if (suijishu==num) {
			System.out.println("你猜对啦！！！");
		}else {
			System.out.println("你猜的大了一点");
		}
	}
	if (count==1) {
		System.out.println("你真是个大神");
	}else if (count>=2&&count<=5) {
		System.out.println("你真是个天才");
	}else if (count>=6&&count<=7) {
		System.out.println("普通人，你好啦");
	}else if (count>=8) {
		System.out.println("哦买噶的，你太艰辛了！");
	}
}
```

### 5、作业：

**1.从控制台输入一个数字，算出这个数字所对应的【阶乘】**

```java
public static void main(String[] args) {
	// TODO 自动生成的方法存根
		int count=0;
		Scanner scanner=new Scanner(System.in);
		count=scanner.nextInt();
		System.out.println("请输入求阶乘的数：");
		int i=1;
		int sum=1;
		while (count>=i) {
			sum=sum*i;
			i++;
		}
		System.out.println(sum);
		
}
```
**2.从控制台输入一个数字，判断这个数字是不是一个【素数】**

```java
public static void main(String[] args) {
			int count=0;
			Scanner scanner=new Scanner(System.in);
			count=scanner.nextInt();	
			int myfalse=0;
			if (count>=4) {
				for (int i = 2; i < count; i++) {
					if (count%i==0) {				
						myfalse++;	
					}			
			    }	
				if (myfalse>0) {
					System.out.println("这个数不是素数");
				}else {
					System.out.println("这个数是是素数");
				}	
			}else if (count==1) {
				System.out.println("这个数不是素数");

			}else {
				System.out.println("这个数是素数");
				
			}
			
		}


```



## 第三节	数组

### 1、讲义

| 数组 |                                                    |
| ---- | -------------------------------------------------- |
|      | 在内存空间中开辟出来的一块连续空间，用来存储一组值 |

| 数组声明及使用的步骤 |            |                                            |
| -------------------- | ---------- | ------------------------------------------ |
|                      | 1.声明     | 在内存中声明数组，指定【数组名】           |
|                      | 2.开辟空间 | 在内存中开辟出指定数字的空间               |
|                      | 3.赋值     | 开辟空间后，数组中会有默认值，也可以自定义 |
|                      | 4.使用     | 输出或运算                                 |

| 数组使用技巧 |                                                   |                                                              |
| ------------ | ------------------------------------------------- | ------------------------------------------------------------ |
|              | 1.2步骤合并(声明的同时开辟空间)                   | int nums[] = new int[5];                                     |
|              | 1.2.3步骤合并（声明的同时开辟空间，并且赋初始值） | int nums[] = new int[]{1,3,5,7,9};                               int nums[] = {1,3,5,7,9}; |

一个变量可以放一个值，一个数组可以放多个值，一个集合可以放多个数组

### 2、学习代码

```java
public static void main(String[] args) {
		//声明
		int nums[];
		String[] names;
			

		//开辟空间
		nums=new int[5];
		names=new String[3];
		
		Double[] doubles=new Double[5]; 		//声明+开辟空间
		
		//赋值
		nums[1]=20;
		nums[3]=60;
		
		names[1]="张三";
		
		doubles[1]=3.33333;
		
    	//声明+开辟空间+赋值
		int[] sum={1,2,3};
		String[] strings=new String[]{"张三","李四","王五"};
		
		//使用
		System.out.println(nums[0]);
		System.out.println(nums[1]);
		System.out.println(nums[2]);
		System.out.println(nums[3]);
		System.out.println();
		
		System.out.println(names[0]);
		System.out.println(names[1]);
		System.out.println(names[2]);
		System.out.println();
		
		System.out.println(doubles[0]);
		System.out.println(doubles[1]);
		//输出数组长度
		System.out.println("strings的长度："+strings.length);
		
		//遍历输出
		for (int i = 0; i < strings.length; i++) {
			String string = strings[i];
			System.out.println(string);	
		}
		
		for (Integer num : sum) {
			System.out.println(num);
		}
	}


```

**输出方式：**

```java
public static void main(String[] args) {
	int[] num={1,2,3,4,5,6,7};
	//正序输出
	for (int i = 0; i < num.length; i++) {
		System.out.print(num[i]);
	}
	System.out.println();
	//倒序输出
	for (int i = num.length-1; i >=0; i--) {
		System.out.print(num[i]);
	}
	System.out.println();
	//倒序输出中间3位
	for (int i = num.length-3; i >=2; i--) {
		System.out.print(num[i]);
	}
	System.out.println();
	//正序隔位输出
	for (int i = 0; i < num.length; i+=2) {
		System.out.print(num[i]);
	}
	System.out.println();
	//输出偶数位
	for (int i = 1; i < num.length; i+=2) {
		System.out.print(num[i]);
	}
	System.out.println();
}
```

## 第四节	Char和Int之间转换得小应用（数组，循环综合运用）

### 1、加密解密小程序

```java
public class Main {
	public static void main(String[] args) {
		//创建控制台输入对象
		Scanner input=new Scanner(System.in);
		while (true) {
			//提示
			System.out.println("*************************************");
			System.out.println("1.加密");
			System.out.println("2.解密");
			System.out.println("3.退出");
			System.out.println("*************************************");
			//程序开始，选择功能
			System.out.println("请选择：");
			//输入功能选项
			int choice=input.nextInt();
			if (choice==1) {
				//加密
				System.out.println("请输入加密文字：");
				String str=input.next();
				System.out.println("请输入加密密码");
				int num=input.nextInt();
				//创建一个新的字符串变量
				String newStr="";
				//将str字符串变成char数组
				char[] c=str.toCharArray();
				for (int i = 0; i < c.length; i++) {
					//定义一个变量temp，将char类型的元素转化成int类型，并存储到temp中
					int temp=c[i];
					//使用密码加密数字
					temp+=num;
					//给字符加%隔开字符
					newStr+="%"+temp;	
				}
				//截取字符串，去掉第一个字符前的百分号
				newStr=newStr.substring(1);
				//输出加密后的字符串
				System.out.println("加密后的文字为：");
				System.out.println(newStr);			
			}else if (choice==2) {
				//解密
				System.out.println("请输入解密文字：");
				String str=input.next();
				System.out.println("请输入解密密码：");
				int num=input.nextInt();
				//定义一个字符串变量
				String newStr="";
				//按百分号进行分割，存储到arr数组中
				String[] arr=str.split("%");
				for (int i = 0; i < arr.length; i++) {
					//定义一个变量temp，将string类型的元素转换成int类型,并存储到temp中
					int temp=Integer.parseInt(arr[i]);
					//使用密码进行解密
					temp-=num;
					//将int类型的元素转化为char类型
					char c=(char)temp;
					//将字符连接成字符串
					newStr+=c;
				}
				//输出字符串
				System.out.println("解密后的文字为：");
				System.out.println(newStr);
			}else if (choice==3) {
				//退出程序
				System.out.println("程序结束，谢谢使用！");
				break;
			}else {
				System.out.println("是不是傻，您输入的数字错误，没有此选项！");
			}
		}
	}
```

## 第五节	双重循环

### 1、讲义

| 二重循环 |                                            |
| -------- | ------------------------------------------ |
|          | 一个完整的循环中，包含另一个完整的循环结构 |
|          | for(int I = 0; I < 3; i++){                |
|          | for(int j = 0; j < 5; j++){                |
|          | }                                          |
|          | }                                          |
|          | 总结：外层循环1次，内层循环N次             |

## 第六节	面向对象

### 1、讲义

| Java中的命名法         |                                         |                                                        |                                                              |                        |          |
| ---------------------- | --------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ | ---------------------- | -------- |
|                        | 驼峰命名法                              | 第一个单词首字母小写，第二个单词开始，首字母大写       | liuMinGe                                                     |                        |          |
|                        | 帕斯卡命名法                            | 所有单词首字母均大写                                   | LiuMinGe                                                     |                        |          |
|                        | 驼峰命名法                              | 包名                                                   | 属性                                                         | 方法                   | 局部变量 |
|                        | 帕斯卡命名法                            | 项目名                                                 | 类名                                                         | 接口名                 |          |
| Java中方法的编辑和使用 |                                         |                                                        |                                                              |                        |          |
|                        | 访问修饰符 返回类型   方法名(参数列表){ |                                                        |                                                              |                        |          |
|                        | 方法主体                                |                                                        |                                                              |                        |          |
|                        | }                                       |                                                        |                                                              |                        |          |
|                        | 访问修饰符                              |                                                        |                                                              |                        |          |
|                        |                                         | public                                                 | 公有的                                                       | 外部和本类内部均可访问 |          |
|                        |                                         | private                                                | 私有的                                                       | 只允许本类内部访问     |          |
|                        | 返回类型                                |                                                        |                                                              |                        |          |
|                        |                                         | void                                                   | 无返回                                                       |                        |          |
|                        |                                         | int                                                    | 必须返回（return）一个整型的值                               |                        |          |
|                        |                                         | 案例                                                   |                                                              |                        |          |
|                        |                                         |                                                        | public int jia(){                                            |                        |          |
|                        |                                         |                                                        | int num3 = num1 + num2;                                      |                        |          |
|                        |                                         |                                                        | return num3;                                                 |                        |          |
|                        |                                         |                                                        | }                                                            |                        |          |
|                        |                                         |                                                        | int a1 = c.jia();                                            |                        |          |
|                        | 参数                                    |                                                        |                                                              |                        |          |
|                        |                                         | 形参                                                   | 定义方法时所使用的参数，语法：数据类型 名                    |                        |          |
|                        |                                         |                                                        | public void da(String  name){     //String name是形参，形参：数据类型 变量名 |                        |          |
|                        |                                         |                                                        | System.out.println("打" +  name);                            |                        |          |
|                        |                                         |                                                        | }                                                            |                        |          |
|                        |                                         | 实参                                                   | 调用方法时所使用的参数，变量名或值                           |                        |          |
|                        |                                         |                                                        | zs.da(name);                                                 |                        |          |
|                        |                                         | 注意点：使用带参方法时，参数的个数，类型，顺序必须一致 |                                                              |                        |          |
| Java方法调用图解       |                                         |                                                        |                                                              |                        |          |
|                        | Test类                                  |                                                        |                                                              |                        |          |
|                        |                                         | int num1 = 10;                                         |                                                              |                        |          |
|                        |                                         | int num2 = 20;                                         |                                                              |                        |          |
|                        |                                         | int num3 =    c.jia(num1, num2);                       |                                                              |                        |          |
|                        |                                         |                                                        |                                                              |                        |          |
|                        | Calc类                                  |                                                        |                                                              |                        |          |
|                        |                                         |                                                        | public int jia(int num1, int num2){                          |                        |          |
|                        |                                         |                                                        | return num1 + num2;                                          |                        |          |
|                        |                                         |                                                        | }                                                            |                        |          |

## 第七节	方法

### 1、讲义

| 重载方法 |                                                              |
| -------- | ------------------------------------------------------------ |
|          | 在同一个类中，方法名相同，参数项不同（参数类型，参数个数）   |
|          | 系统调用时将根据参数项选择调用的方法                         |
|          | 例子：                                                       |
|          | public void show(String name){}                              |
|          | public void show(int  age){}                                 |
| 构造方法 |                                                              |
|          | 在一个类中，方法名和类名相同，没有返回类型的方法             |
|          | 例子：                                                       |
|          | public Student(){}                                           |
|          | 构造方法在初始化对象时，通过【new】关键字调用                |
|          | 如果没有【自定义】构造方法，程序将会默认分配一个【隐式】【无参】的构造方法 |
|          | 构造方法也可以重载                                           |

## 第八节	集合

### 1、讲义

| Java中的实体类 |                         |
| -------------- | ----------------------- |
|                | 创建实体类的步骤        |
|                | 1.编写私有的属性        |
|                | 2.生成公有的get/set方法 |
|                | 3.生成无参/有参构造     |

| Java集合体系 | List | ArrayList | 0     | 1    | 2    |
| ------------ | ---- | --------- | ----- | ---- | ---- |
|              |      |           | a     | b    | c    |
|              | Set  |           |       |      |      |
|              |      |           |       |      |      |
|              | Map  | HashMap   | key   |      | key  |
|              |      |           | value |      | c    |
|              |      |           |       | key  |      |
|              |      |           |       | b    |      |

| ArrayList集合 |              |                                                |
| ------------- | ------------ | ---------------------------------------------- |
|               | 集合声明     | ArrayList<类型> list =  new ArrayList<类型>(); |
|               | 添加集合元素 | list.add(元素);                                |
|               | 获取集合长度 | list.size();                                   |
|               | 获取单个元素 | list.get(下标);                                |
|               | 循环集合     | for形式                                        |
|               |              | foreach形式                                    |
|               | 删除集合元素 | list.remove(下标);                             |
|               |              | list.remove(对象名);                           |
|               |              | list.clear();                                  |

| HashMap集合 |              |                                                              |
| ----------- | ------------ | ------------------------------------------------------------ |
|             | 集合声明     | HashMap<键类型, 值类型> hm  = new HashMap<键类型, 值类型>(); |
|             | 添加集合元素 | hm.put(键, 值); 添加的时候指定键和值                         |
|             | 获取集合长度 | hm.size();                                                   |
|             | 获取单个元素 | hm.get(键);  通过键来获取元素                                |
|             | 循环集合     | foreach形式                                                  |
|             | 删除集合元素 | hm.remove(键); 通过键来删除元素                              |
|             |              | hm.clear();                                                  |

## 第九节	面向对象

### 1、封装

构造方法不可以继承，但是可以调用

| 封装 |                                                              |                                                              |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ |
|      | 面向对象的第一大特征，从事物中抽取共同特征，写入到一个类的过程 |
|      | 数据类封装                                                   | 封装一个实体类，里面包含【私有属性】【公有get/set方法】【无参/有参构造】 |
|      | 业务类封装                                                   | 封装一个业务功能类，里面包含若干方法（带参数和返回）         |

### 2、继承

| 继承 |                                                  |                                                              |                                      |
| ---- | ------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------ |
|      | 面向对象的第二大特征，用于减少代码冗余，实现复用 |                                                              |                                      |
|      | 角色                                             | 父类                                                         | 基类                                 |
|      |                                                  | 子类                                                         | 派生类/衍生类                        |
|      | 关系                                             | 子类   继承 父类                                             |                                      |
|      | 语法                                             | 子类   extends 父类                                          |                                      |
|      | 判断方法                                         | is-a                                                         | 子类 is a 父类                       |
|      | 继承特性                                         | 单根性                                                       | 一个类只能继承一个父类               |
|      |                                                  | 传递性                                                       | 从父类继承的成员可以被其子类再次继承 |
|      | 继承过程中【构造方法】的调用                     |                                                              |                                      |
|      |                                                  | 在继承关系下，子类的构造方法会默认的调用【父类无参】构造方法 |                                      |
|      |                                                  | 通过super();方法，可以指定调用【父类有参】构造方法           |                                      |
|      |                                                  | super();必须写在方法中的第一行                               |                                      |
|      | 继承过程中的重写                                 |                                                              |                                      |
|      |                                                  | 父类方法不满足子类要求的时候                                 |                                      |
|      |                                                  | 父类                                                         | public void show(){}                 |
|      |                                                  | 子类                                                         | public void show(){}                 |

### 3、多态

| 同一个方法在不同类中所具有的不同表现形式 |                                            |                  |                              |
| ---------------------------------------- | ------------------------------------------ | ---------------- | ---------------------------- |
| 实现多态的步骤                           |                                            |                  |                              |
|                                          | 1                                          | 必须要有继承关系 |                              |
|                                          | 2                                          | 子类重写父类方法 |                              |
|                                          | 3                                          | 父类指向子类引用 |                              |
| 多态使用的4个场景                        |                                            |                  |                              |
|                                          | 以【父类类型】作为【对象类型】             |                  |                              |
|                                          | 以【父类类型】作为【集合类型】             |                  |                              |
|                                          | 以【父类类型】作为【参数类型】             |                  |                              |
|                                          | 以【父类类型】作为【返回类型】             |                  |                              |
| 重写分类                                 |                                            |                  |                              |
|                                          | 普通方法重写（【部分】子类重写父类方法）   |                  |                              |
|                                          |                                            | 父类             | public void show(){}         |
|                                          |                                            | 子类             | public void show(){}         |
|                                          | 抽象方法重写（【所有】子类都重写父类方法） |                  |                              |
|                                          |                                            | 父类             | public abstract void show(); |
|                                          |                                            | 子类             | public void show(){}         |

### 4、接口

| 接口Interface |                                                        |                        |                                        |            |
| ------------- | ------------------------------------------------------ | ---------------------- | -------------------------------------- | ---------- |
|               | 一种特殊的抽象父类：代表的是一种能力，用来规范类的行为 |                        |                                        |            |
|               |                                                        | 角色                   | 接口                                   |            |
|               |                                                        |                        | 实现类                                 |            |
|               |                                                        | 关系                   | 实现类 实现 接口                       |            |
|               |                                                        | 语法                   | 实现类 implements 接口                 |            |
|               |                                                        | 接口特性               | 多实现：一个类可以【实现多个】接口     |            |
|               |                                                        | 继承和接口可以同时存在 |                                        |            |
|               |                                                        |                        | 先继承，后实现                         |            |
|               |                                                        |                        | public  class C extends A implements B |            |
|               | 类，接口之间的关系                                     |                        |                                        |            |
|               |                                                        | 类与类之间的关系       |                                        |            |
|               |                                                        |                        | 关系                                   | 继承       |
|               |                                                        |                        | 特性                                   | 单继承     |
|               |                                                        |                        | 关键字                                 | extends    |
|               |                                                        | 类与接口之间的关系     |                                        |            |
|               |                                                        |                        | 关系                                   | 实现       |
|               |                                                        |                        | 特性                                   | 多实现     |
|               |                                                        |                        | 关键字                                 | implements |
|               |                                                        | 接口与接口之间的关系   |                                        |            |
|               |                                                        |                        | 关系                                   | 继承       |
|               |                                                        |                        | 特性                                   | 多继承     |
|               |                                                        |                        | 关键字                                 | extends    |