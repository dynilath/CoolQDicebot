DiceRobot kills you 3000
-----
Just a simple dicebot for coolq in development.<br> 
只是一个简单的酷Q骰子机器人。<br> 
[下载cpk](https://github.com/decterous/CoolQDicebot/releases/latest)<br> 
[获取酷Q](https://cqp.cc/)<br> 

使用示范
-----

1.多行输入<br>
>输入

<pre><code>     .  r1d10 测试1
   .   r 2d10 测试2
 .r      3d10 测试3</code></pre>
>输出

<pre><code> * 测试 测试1 掷骰: 1d10 = (7) = 7 
 * 测试 测试2 掷骰: 2d10 = (5 + 7) = 12
 * 测试 测试3 掷骰: 3d10 = (5 + 3 + 4) = 12 </code></pre>
<br> 

2.算式输入<br> 
>输入

<pre><code>.r 1d20+1d6-3+4+11 破邪斩+猛力攻击
.r 5d4*3/4
.r 5d4*2d2+3+4/3</code></pre>
>输出

<pre><code> * 测试 破邪斩+猛力攻击 掷骰: 1d20+1d6-3+4+11 = (19) + (6) - 3 + 4 + 11 = 37
 * 测试  掷骰: 5d4*3/4 = (2 + 2 + 2 + 2 + 2) * 3 / 4 = 7.5
 * 测试  掷骰: 5d4*2d2+3+4/3 = (1 + 4 + 3 + 4 + 2) * (2 + 2) + 3 + 4 / 3 = 60.3333 </code></pre>
<br>


3.多骰取部分<br> 
>输入

<pre><code>.r 4d6k3 力量属性
.r 2d20kl1+11 降祸攻击</code></pre>
>输出

<pre><code> * 测试 力量属性 掷骰: 4d6k3 = (4 + 4 + 5 + (2)) = 13
 * 测试 降祸攻击 掷骰: 2d20kl1+11 = (11 + (15)) + 11 = 22</code></pre>
<br> 

4.修改昵称（现在支持多行输入了，并且取消了对多行昵称的支持）<br> 
>输入

<pre><code>.n 新的名字</code></pre>
>输出

<pre><code> * Da'Inihlus 的新名字是  新的名字</code></pre>
<br> 

5.无返回文字地修改昵称<br> 
>输入

<pre><code>.ns 迷诱魔
.r 1d20+20
.ns 反pal魅魔破善斩
.r 1d20+24</code></pre> 
>输出

<pre><code> * 迷诱魔  掷骰: 1d20+20 = (15) + 20 = 35
 * 反pal魅魔破善斩  掷骰: 1d20+24 = (12) + 24 = 36</code></pre> 

6.coc7的特殊d100规则<br> 
(刷了好多次才有这个个位是0的结果)<br>
>输入

<pre><code>.cb5闪避(50)
.cp2闪避(50)
.cp5b5b2我也不知道为什么会这样骰
.cp5b5pd奖罚抵消
.cb4如果个位是0</code></pre>
>输出

<pre><code> * goubi 闪避(50) 掷骰: d100b5 = [(5) + (9) + (5) + (3) + 0 + (5)] [4] = 4
 * goubi 夹击闪避(50) 掷骰: d100p2 = [(5) + 6 + (3)] [4] = 64
 * goubi 我也不知道为什么会这样骰 掷骰: d100p5b5b2 = d100b2 = [(9) + 0 + (2)] [9] = 9
 * goubi pd奖罚抵消 掷骰: d100p5b5 = 33
 * goubi 如果个位是0 掷骰: d100b4 = [(2) + (6) + (10) + 2 + (4)] [0] = 20</code></pre>
<br> 


特性
-----
所有的骰子指令支持多行输入<br> 
骰子指令的头部.r可以任意填充空格，例如"      .    r     1d20"也是有效的<br> 
骰子用昵称每个群每个qq不同，保存在数据库不会断电丢失<br> 
