# 小專案：Matching Game

### 定義Class

```python
class Card:
    num = 0
    is_open = False


row = 2
col = 3

nums = [
    [8, 5, 3],
    [5, 3, 8],
]

cards: list[list[Card]] = []
for i in range(row):
    card_row = []
    for j in range(col):
        new_card = Card()
        new_card.num = nums[i][j]
        card_row.append(new_card)
    cards.append(card_row)

# print(cards)
# cards = [
#   [Card(), Card(), Card()],
#   [Card(), Card(), Card()],
# ]


def show(cards: list[list[Card]]):
    for i in range(row):
        for j in range(col):
            if cards[i][j].is_open:
                print(cards[i][j].num, end="")
            else:
                print("%", end="")
        print()


show(cards)
while True:
    print("哈囉 請輸入你要翻的牌面 噗噗噗噗噗噗噗噗噗噗噗")
    r, c = map(int, input().split())
    cards[r][c].is_open = True
    show(cards)

```

### 加入Method

把show做成Card的method，另外做一個show\_table

並完成剩下的遊戲邏輯

```python
class Card:
    num: int
    # 'close', 'open', 'match'
    status: str = "close"

    def show(self):
        if self.status == "close":
            print("#", end='')
        elif self.status == "open":
            print(self.num, end='')
    
row = 2
col = 3

cards: list[list[Card]] = []
# cards = []

nums = [
    [8, 3, 5],
    [5, 3, 8],
]
# 創造牌面
for i in range(row):
    new_row = []
    for j in range(col):
        new_card = Card()
        new_card.num = nums[i][j]
        new_row.append(new_card)
    cards.append(new_row)



def show_table(cards: list[list[Card]]):
    for i in range(row):
        for j in range(col):
            cards[i][j].show()
        print()
    print()

# 已翻的牌數 = 0
while ...:
    # x1, y1 讓使用者輸入他想要翻的牌1
    # 讓他看他翻的牌是什麼
    # cards[x1][y1].status = 'open'
    # show_table(cards)

    # x2, y2 讓使用者輸入他想要翻的牌2
    # 讓他看他翻的牌是什麼

    input('請按任意鍵繼續')

    # 如果這兩張牌有match
    # 就把這兩張牌設為match
    # 紀錄目前已翻的牌數

    # 如果沒有match
    # 把兩張牌蓋起來

    # 如果翻完，就結束遊戲

    

# cards[0][0].status = 'open'
# show_table(cards)

# cards[0][1].status = 'open'
# show_table(cards)

```

### 參考

```python
class Card:
    num: int
    # 'close', 'open'
    status: str = "close"

    def show(self):
        if self.status == "close":
            print("#", end='')
        elif self.status == "open":
            print(self.num, end='')
    
row = 2
col = 3

cards: list[list[Card]] = []
# cards = []

nums = [
    [8, 3, 5],
    [5, 3, 8],
]
# 創造牌面
for i in range(row):
    new_row = []
    for j in range(col):
        new_card = Card()
        new_card.num = nums[i][j]
        new_row.append(new_card)
    cards.append(new_row)



def show_table(cards: list[list[Card]]):
    print()
    for i in range(row):
        for j in range(col):
            cards[i][j].show()
        print()
    print()

match = 0
while True:
    show_table(cards)

    x1, y1 = map(int, input('請輸入第一張牌: ').split())
    cards[x1][y1].status = 'open'
    show_table(cards)
    
    x2, y2 = map(int, input('請輸入第二張牌: ').split())
    cards[x2][y2].status = 'open'
    show_table(cards)

    input('請按任意鍵繼續')

    if cards[x1][y1].num == cards[x2][y2].num:
        match += 2
    else:
        cards[x1][y1].status = 'close'
        cards[x2][y2].status = 'close'
        

    if match == row * col:
        print('You Win!')
        break

```
