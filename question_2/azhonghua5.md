```
import random
'''
系统随机生成一个1~100之间的整数，
玩家有5次机会，每猜一次系统就会提示玩家该数字是偏大还是偏小，
如果猜中了，则告知玩家并提前结束游戏，如果5次都没猜中，结束游戏并告知正确答案。
'''
rand_num = random.randint(1, 100)
for i in range(0, 5):
    num = input("请输入数字：")
    if i == 4:
        if num == rand_num:
            print("恭喜你，猜中数字！")
            break
        else:
            print("游戏结束，正确答案是%s" %rand_num)
            break

    if num == rand_num:
        print("恭喜您，猜中数字！")
    elif int(num) < rand_num:
        print("回答错误，您猜的数字小了，您还有%s次机会！" %(4 - i))
    else:
        print("回答错误，您猜的数字大了，您还有%s次机会！" %(4 - i))

```
