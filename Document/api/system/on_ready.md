#系统就绪事件
***
##函数声明
```
void on_ready(void);
```

***
##函数功能
在蓝牙模块已经开始发送广播后由系统调用。  
用于可处理在开始广播后的任务。

***
##函数参数
参数    | 数据类型   | 说明
:----- | :-------- | :------
*返回值*  | void      | 无

***
##函数举例
```
	...
	
	//当前的函数
	void on_ready()
	{
		gpio_setup(LED_1, GPIO_OUTPUT);		//设置一个引脚模式
		run_after_delay(led_on_task, NULL, 100);    //100m后运行
	}
	
	...
```