---
title: Real面试真题
tags: Interview面试
date: 2023-09-11
---
在这个系列里面，我将分享一些之前的面试真题

#### 一、有三个人，从0到100选数字。每个人选一个数字，并拿到该数字对应的积分。数字对应积分的规则是，若甲选了50，乙选了49，丙选了51，那甲拿到(50-49)/2+(51-50)/2，乙拿到49+(50-49)/2，丙拿到(100-51)+(51-50)/2。若你拿的数字是最大的那个，那你可以积分到你到100的距离加上你和最近一个别人选的数字的距离的一半。每个人都会拿使他分数最高的那个数字，问你第一个选，你要选数字几使得你的分数最大



首先，我们需要找到一个数字，使得你的分数最大。根据规则，你的分数等于你到100的距离加上你和最近一个别人选的数字的距离的一半。

让我们用符号来表示这个问题。假设你选择的数字是x，甲、乙、丙选择的数字分别是a、b、c。那么你的分数可以表示为：

```
score = (100 - x) + (x - max(a, b, c)) / 2
```

为了使得你的分数最大，我们需要找到一个x，使得score取得最大值。

让我们来解决这个问题。首先，我们可以观察到score是关于x的一个凹函数。也就是说，score在某个点左边是递增的，在某个点右边是递减的。因此，我们只需要找到score取得最大值的那个点。

根据题目描述，x的取值范围是0到100之间。因此，我们只需要计算score在x=0和x=100处的值，然后比较它们。

当x=0时，score等于100 + (0 - max(a, b, c)) / 2。 当x=100时，score等于0 + (100 - max(a, b, c)) / 2。

因此，我们只需要比较max(a, b, c)在0和100之间的大小即可。

希望这个解答对你有帮助！如果你还有其他问题，请随时提问。

####  二、A B C 三个人相互射击， A B C 命中率分别为 30% 50% 100% ，每轮每个人可以任选一个人射击或者什么也不做，开枪是同时的；请问，每个人都为了保证自己存活率更高的情况下，射击的情况以及每个人的存活概率？





