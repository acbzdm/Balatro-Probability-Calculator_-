# 小丑牌成功概率计算器

## 项目简介

小丑牌成功概率计算器是一个用 Python 开发的应用程序，用于计算特定条件下弃牌后做成目标牌型的成功的概率。
用户输入需要牌的数量，弃牌后的获得牌数和牌剩余数量将返回成功的概率。

## 计算公式

举例示意
现有牌做顺子差一张。弃掉剩下的4张牌后至少来一张9或A才能做出顺子
需要牌的剩余总数为8，需要牌的至少数量1，弃牌后收到的牌数4，剩余牌数44。

$$\begin{align\\*}
\frac{C_{8}^{1}*C_{36}^{3}}{C_{44}^{4} } +\frac{C_{8}^{2}*C_{36}^{2}}{C_{44}^{4} } +\frac{C_{8}^{3}*C_{36}^{1}}{C_{44}^{4} }+\frac{C_{8}^{4}*C_{36}^{0}}{C_{44}^{4} }
\end{align\\*}$$

$$\begin{align\\*}
\frac{9}{6}
\end{align\\*}$$

Python
使用scipy.special里的comb函数计算排列组合。使用tkinter做可视化输入输出

效果展示
![作顺子的概率为56 61%](https://github.com/user-attachments/assets/23a3be6d-26a8-4a58-a0eb-185c9cd5307a)
做顺子的概率为56.61%

![作红桃同花的概率为31 67%](https://github.com/user-attachments/assets/fe1e9de3-5cb6-4042-b4ba-416388f61959)
做红桃同花的概率为31.67%

![弃牌做红心同花后做红心同花的概率38 12%](https://github.com/user-attachments/assets/558b6b65-13c7-4ada-b4c2-60e96f1541fd)
弃牌做红心同花后做红心同花的概率38.12%，比31.67%并没有上升多少

![弃牌作红心同花后作方块同花的概率为56 28%](https://github.com/user-attachments/assets/964d13c7-929b-4092-9fd5-15981b0b5db4)
弃牌做红心同花后做方块同花的概率为56.28%

![弃牌做红心同花后做小顺子的概率56 28%](https://github.com/user-attachments/assets/39957ddc-c355-4655-9aec-79da880eb316)
弃牌做红心同花后做小顺子的概率56 28%

![弃牌做红心同花后做大顺子的概率50 25%](https://github.com/user-attachments/assets/2000128a-18b6-4b1a-9158-68c37db19fca)
弃牌做红心同花后做大顺子的概率50.25%

此时做方块同花和小顺子的概率相同，但是同花的得分会更高。

还有时会出现顺子，同花，葫芦都各差一张做成时使用该计算器计算更加快捷。


## 使用说明





1. 打开应用程序。
2. 输入以下参数：
   - **需要牌的剩余总张数**：输入总牌数。
   - **需要牌的至少数量**：输入需要的最小牌数。
   - **弃牌后收到的牌数**：输入弃牌后实际得到的牌数。
   - **剩余牌总数**：输入剩余牌的总数。

3. 点击“开始计算”按钮查看结果。

## 界面预览

![应用程序界面](C:\Users\黄敬生\Desktop\作红桃同花的概率为31.67%.png)

## 安装与运行

### 依赖项

确保安装以下依赖：

- Python 3.x
- Kivy

### 克隆项目

```bash
git clone https://github.com/你的用户名/小丑牌成功概率计算器.git
cd 小丑牌成功概率计算器
