Pyspark Streaming Consume Kafka Data and Put into Hbase  
===================================  
  The project is for use Pyspark Streaming to real-time consumption of Kafka data<br />  
    
  
The Implementation Process Of Project  
-----------------------------------  
  Include the priciple of frame and code<br />   
    
### Framework of Porject  
 1.Spark2.1 , kafka1.0 , python2.7 ,hbase0.98<br />
 2.Spark-Streaming have two method to cunsume kafka data<br />   
      > first is Receive-base method as same as Storm,real-time read cache_data to memory<br />  
      > second is Direct method at regular time  to read data<br /> 
     
### Core_Code of Project
    lines = KafkaUtils.createDirectStream(ssc,topic,kafkaParams={"metadata.broker.list":brokers})
    with table.batch(batch_size=1000) as b:
            b.put((line.label),{
                b'label:itemtype': (line.label),
                b'infomation:url': (str(line.value)),})

    
    
The conclusion Of Project  
----------------------------------- 
> * this project is failed when submit spark on yarn
           
### 链接  
1.[点击这里你可以链接到www.google.com](http://www.google.com)<br />  
2.[点击这里你可以链接到www.baidu.com](http://www.baidu.com)<br />  

###只是显示图片  
![github](http://github.com/unicorn.png "github")  
  
###想点击某个图片进入一个网页,比如我想点击github的icorn然后再进入www.github.com  
[![image]](http://www.github.com/)  
[image]: http://github.com/github.png "github"  
  
### 文字被些字符包围  
> 文字被些字符包围  
>  
> 只要再文字前面加上>空格即可  
>  
> 如果你要换行的话,新起一行,输入>空格即可,后面不接文字  
> 但> 只能放在行首才有效  
  
### 文字被些字符包围,多重包围  
> 文字被些字符包围开始  
>  
> > 只要再文字前面加上>空格即可  
>  
>  > > 如果你要换行的话,新起一行,输入>空格即可,后面不接文字  
>  
> > > > 但> 只能放在行首才有效  
  
### 特殊字符处理  
有一些特殊字符如<,#等,只要在特殊字符前面加上转义字符\即可<br />  
你想换行的话其实可以直接用html标签\<br /\> 
