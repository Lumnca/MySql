# :rocket:mysql函数	 #

:arrow_down:[数学函数](#a1)


<p id="a1"></p>

### :round_pushpin:数学函数 ###

数学函数主要用来处理数据，其包括绝对值函数，三角函数，对数函数，随机数函数，在有错误产生时，数学函数将会返回空值NULL。

**:arrow_up_small:ABS(x)** ：返回X的绝对值

```sql
select ABS(5),ABS(-7),ABS(-2.66);
```

**:arrow_up_small:SQRT(x)** : 返回x平方根

```sql
select SQRT(81),SQRT(8);
```

**:arrow_up_small:MOD(x,y)** : x对于y求余

```sql
select MOD(7,3);   //1

select MOD(7.5,3)  //1.5
```

**:arrow_up_small:CEIL(x),CEILING(x)** :  对x向上取整，及大于这个数的最小整数

```sql
select CEIL(12.2),CEIL(-2.6);       //13,2
```


**:arrow_up_small:FLOOR(x)** : 向下取整，即小于这个数的最大整数

```sql
select FLOOR(3.89),FLOOR(-1.22);   //3,-2
```

**:arrow_up_small:RAND(x)** :获取随机数函数

没有参数时的rand()产生一个0~1的随机数。可以利用这个来随机生成一个数：

```sql
select CEIL(RAND()*100);   //生成1到100的数
```

含有参数代表随机数生成的序号，如下面，序号为1的两个随机数相等：

```sql
select CEIL(RAND(1)*100),CEIL(RAND(1)*100),CEIL(RAND(2)*100);
```

**:arrow_up_small:ROUND(x,y)** : 对x四舍五入，保留y位小数，若不含y参数四舍五入为整数。

```sql
select ROUND(5.265),ROUND(5.3398,3);  //5,5.340
```

**:arrow_up_small:TRUNCATE(x,y)** : 截取x小数后y位小数,必须含有y参数

```sql
select TRUNCATE(1.99,1),TRUNCATE(1.99,2),TRUNCATE(1.99,3);  //1.9,1.99,1.990
```

**:arrow_up_small:SIGN(x)** : 返回x的符号，正，零，负为1,0，-1

```sql
select SIGN(5),SIGN(0),SIGN(-5.3);         //1,0,-1
```

**:arrow_up_small:幂运算POW(x,y),POWER(x,y),EXP(x)** : 前面两个都是返回x的y次方，EXP(x)代表返回e的x次方。

```sql
select POW(2,3),POWER(4,-1),EXP(2);
```

**:arrow_up_small:对数运算LOG(x),LOG10(x)** : 前面返回以e为底的x自然数对数，后面是以10为底的自然数对数

```sql
select LOG(EXP(2)), LOG10(100);   //2,2
```

**:arrow_up_small:三角函数**

由于三角函数使用较少，这里没有列出，有兴趣可以参考文献资料。






