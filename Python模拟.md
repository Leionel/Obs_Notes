根据您提供的《数据结构与程序设计 (Python语言)》期末考试范围说明（PDF第一页）以及配套教学课件，我为您设计了两套期末模拟试题。

**出题原则：**
1.  **严格遵守考纲：** 不考复数、位运算、match语句、嵌套函数、装饰器、继承、多态、生成器、异常处理。
2.  **库的使用：** 重点考察 `math` 和 `random`，其他库（如 pandas, matplotlib, jieba, turtle）仅考察名称和应用场景。
3.  **题型结构：** 单选 (30分) + 简答 (10分) + 改错 (10分) + 编程 (50分) = 100分。

---

### 模拟试题 A 卷（难度：适中）
**适用对象：** 考察基础知识掌握情况，适合绝大多数学生进行自测。

#### 一、单选题（每题2分，共30分）

1.  下列哪个标识符在 Python 中是合法的？
    A. `2day`   B. `if`   C. `_my_var`   D. `my-var`
2.  执行语句 `print(round(3.5))` 和 `print(int(3.9))` 的结果分别是？
    A. 3, 3   B. 4, 3   C. 4, 4   D. 3, 4
3.  下列关于 Python 字符串的说法，**错误**的是？
    A. 字符串是不可变序列
    B. `s.strip()` 方法可以去除字符串两端的空白字符
    C. `s.replace('a', 'b')` 会直接修改原字符串 `s`
    D. 字符串支持切片操作
4.  已知列表 `lst = [1, 2, 3, 4, 5]`，执行 `lst[1:4]` 的结果是？
    A. `[1, 2, 3]`   B. `[2, 3, 4]`   C. `[2, 3, 4, 5]`   D. `[1, 2, 3, 4]`
5.  在 Python 中，用于生成随机数的标准库是？
    A. `math`   B. `random`   C. `turtle`   D. `pandas`
6.  字典 `d = {'a': 1, 'b': 2}`，执行 `d.get('c', 0)` 的结果是？
    A. 报错   B. None   C. 0   D. 2
7.  下列代码的输出结果是？
    ```python
    a = [1, 2]
    b = a
    b.append(3)
    print(a)
    ```
    A. `[1, 2]`   B. `[1, 2, 3]`   C. `[1, 2, 3, 3]`   D. 报错
8.  要对一个中文文本进行分词，通常使用的扩展库是？
    A. `jieba`   B. `numpy`   C. `flask`   D. `requests`
9.  关于 `open('file.txt', 'w')` 模式，下列说法正确的是？
    A. 如果文件不存在，会报错
    B. 只能读取文件内容
    C. 如果文件已存在，会清空原内容并写入新内容
    D. 追加内容到文件末尾
10. 下列关于 `json` 模块的描述，正确的是？
    A. `json.dumps()` 用于将 Python 对象转换为 JSON 字符串
    B. `json.load()` 用于将 JSON 字符串转换为 Python 对象
    C. `json` 只能处理列表，不能处理字典
    D. `json` 是第三方库，需要单独安装
11. 定义函数时，若想接收任意数量的位置参数，应使用？
    A. `*args`   B. `**kwargs`   C. `args`   D. `&args`
12. 表达式 `[i**2 for i in range(3)]` 的值是？
    A. `[1, 2, 3]`   B. `(0, 1, 4)`   C. `[0, 1, 4]`   D. `[1, 4, 9]`
13. 想要绘制数据可视化图表（如折线图、柱状图），应选择哪个库？
    A. `matplotlib`   B. `requests`   C. `socket`   D. `pickle`
14. 集合（Set）的主要特性是？
    A. 有序且可重复   B. 无序且不重复   C. 有序且不重复   D. 无序且可重复
15. 执行 `import math; print(math.ceil(3.1))` 的结果是？
    A. 3   B. 3.0   C. 4   D. 3.1

#### 二、简答题（10分）

简述 Python 中列表（List）和元组（Tuple）的主要区别，并各列举一个适用的场景。

#### 三、改错题（每题5分，共10分）
*请指出下列代码中的错误并改正。*

**题1：**
```python
# 目的：判断x是否等于10
x = 5
if x = 10:
    print("x是10")
```

**题2：**
```python
# 目的：定义一个类Person，初始化姓名
class Person:
    def init(self, name):  # 错误在这里
        self.name = name

p = Person("Tom")
```

#### 四、编程题（共50分）

1.  **基础运算（10分）：**
    编写程序，计算 1 到 100 之间所有能被 3 整除但不能被 5 整除的整数之和，并输出结果。

2.  **函数与随机数（10分）：**
    编写一个函数 `generate_code(n)`，该函数使用 `random` 模块生成并返回一个由 `n` 个随机大写字母组成的验证码字符串。（提示：大写字母 A-Z 的 ASCII 码范围是 65-90，可用 `chr()` 函数）。

3.  **列表与字典处理（15分）：**
    已知一个包含学生成绩的字典列表：
    `students = [{"name": "Alice", "score": 85}, {"name": "Bob", "score": 72}, {"name": "Cindy", "score": 90}]`
    请编写程序，计算所有学生的平均分，并输出分数最高的学生姓名。

4.  **文件操作与CSV（15分）：**
    假设当前目录下有一个名为 `data.csv` 的文件，内容如下：
    ```
    Name,Age
    Tom,20
    Jerry,18
    ```
    请编写程序：
    1. 读取该文件。
    2. 将每行数据读取并转换为字典格式（例如 `{'Name': 'Tom', 'Age': '20'}`）。
    3. 将这些字典存入一个列表中并打印该列表。

---

### 模拟试题 B 卷（难度：较难）
**适用对象：** 考察对知识点的综合运用能力，逻辑思维能力，适合冲刺高分。

#### 一、单选题（每题2分，共30分）

1.  下列逻辑表达式中，结果为 `True` 的是？
    A. `not (3 > 2)`   B. `3 > 2 and 2 > 3`   C. `'a' in 'apple'`   D. `[]`
2.  `s = "Python"; print(s[::-1])` 的输出结果是？
    A. `Python`   B. `nohtyP`   C. `P`   D. `n`
3.  关于 Python 的内存管理，`a = 10; b = 10; print(id(a) == id(b))` 在通常情况下的结果是？
    A. True   B. False   C. 报错   D. 随机
4.  `lambda x, y: x + y` 定义的是一个？
    A. 生成器   B. 装饰器   C. 匿名函数   D. 递归函数
5.  下列哪个方法**不会**修改列表 `lst` 本身？
    A. `lst.append(1)`   B. `lst.sort()`   C. `lst.reverse()`   D. `sorted(lst)`
6.  使用 `pickle` 模块进行对象序列化时，打开文件的模式应该是？
    A. `'w'`   B. `'wb'`   C. `'r'`   D. `'rb'`
7.  关于 Python 模块中的 `if __name__ == '__main__':`，下列说法正确的是？
    A. 这行代码是语法错误
    B. 只有当模块被导入时，该语句块下的代码才会被执行
    C. 只有当模块被直接运行时，该语句块下的代码才会被执行
    D. 无论何种情况，该语句块下的代码都会执行
8.  已知集合 `A = {1, 2, 3}`，`B = {3, 4, 5}`，则 `A & B` 的结果是？
    A. `{1, 2, 3, 4, 5}`   B. `{3}`   C. `{1, 2}`   D. `{1, 2, 4, 5}`
9.  函数定义 `def func(a, b=2, *args):`，调用 `func(1, 3, 4, 5)` 时，`args` 的值是？
    A. `[4, 5]`   B. `(4, 5)`   C. `4`   D. `(3, 4, 5)`
10. 想要进行科学计算和矩阵运算，通常使用的扩展库是？
    A. `pandas`   B. `numpy`   C. `pygame`   D. `flask`
11. 关于面向对象，以下说法**错误**的是（根据考纲不考继承）：
    A. 类是对象的模板
    B. 对象是类的实例
    C. `__init__` 方法在创建对象时自动调用
    D. 私有属性在 Python 中完全无法在类外部访问
12. 执行 `list(map(lambda x: x*2, [1, 2, 3]))` 的结果是？
    A. `[1, 2, 3]`   B. `[2, 4, 6]`   C. `[1, 4, 9]`   D. 报错
13. `math.floor(-3.5)` 的结果是？
    A. -3   B. -4   C. -3.5   D. 3
14. 字典推导式 `{x: x**2 for x in (2, 4, 6)}` 的结果是？
    A. `[4, 16, 36]`   B. `(4, 16, 36)`   C. `{2:4, 4:16, 6:36}`   D. `{4:2, 16:4, 36:6}`
15. 下列关于 CSV 文件的读写，说法正确的是？
    A. `csv.writer` 写入时必须先写入表头
    B. `csv.reader` 读取的数据默认是字符串列表
    C. CSV 文件只能存储数字
    D. CSV 文件必须用 Excel 打开

#### 二、简答题（10分）

简述 Python 中 `import` 导入模块的机制，并说明 `if __name__ == '__main__':` 的作用及应用场景。

#### 三、改错题（每题5分，共10分）
*请指出下列代码中的错误并改正。*

**题1：**
```python
# 目的：将列表中的字符串转换为整数
lst = ['1', '2', '3']
new_lst = []
for i in lst
    new_lst.append(Integer(i)) # 假设想转换成整型
print(new_lst)
```

**题2：**
```python
# 目的：写入文本到文件
f = open('test.txt', 'w')
f.write(12345)  # 错误在这里
f.close()
```

#### 四、编程题（共50分）

1.  **逻辑与算法（10分）：**
    编写一个函数 `is_prime(n)` 判断一个数是否为素数。利用该函数，输出 100 以内所有的素数，并以列表形式返回。

2.  **字符串与统计（10分）：**
    输入一段英文文本，统计其中每个单词出现的次数（不区分大小写）。
    要求：
    1. 使用字典（或 `collections.Counter`，若允许使用扩展库知识）存储结果。
    2. 按照单词出现次数从高到低打印前 3 个单词及其次数。
    *示例输入：* "Python is good. Python is simple."
    *示例输出：* python: 2, is: 2, good: 1

3.  **面向对象编程（15分）：**
    定义一个名为 `BankAccount` 的类，包含：
    *   属性：`account_number`（账号），`balance`（余额，初始为0）。
    *   方法：
        *   `deposit(amount)`: 存款，余额增加。
        *   `withdraw(amount)`: 取款，如果余额充足则扣除并返回 True，否则打印“余额不足”并返回 False。
        *   `get_balance()`: 返回当前余额。
    请创建对象并演示存款和取款操作。

4.  **综合文件处理（15分）：**
    假设有一个包含多行整数的文本文件 `numbers.txt`（每行一个数字）。
    编写程序：
    1. 读取该文件中的所有数字。
    2. 计算这些数字的总和与平均值。
    3. 将计算结果（总和与平均值）写入到一个新的文件 `result.json` 中，使用 JSON 格式保存，例如 `{"sum": 100, "average": 25.0}`。

---

### 答案解析要点（简略）

**A卷重点：**
*   简答题：列表可变（用 `[]`），元组不可变（用 `()`）。列表用于数据集合，元组用于固定配置或字典键。
*   编程题：注意 `range` 步长、`random.choice` 或字符串拼接、字典遍历、`csv.reader` 或字符串 `split` 处理。

**B卷重点：**
*   简答题：`import` 搜索路径（sys.path），`__main__` 只有在直接运行时为真，用于测试代码防止被导入时执行。
*   编程题：素数判断循环逻辑；字符串 `split` 及 `lower` 处理；类中 `self` 的使用；JSON 的 `dump` 用法及文件读写的 `with open` 习惯。

这份解析包含了**模拟试题 A 卷（适中）**和**模拟试题 B 卷（较难）**的完整答案及详细解析。建议先尝试自己做一遍，再对照解析查漏补缺。

---

### 🟢 模拟试题 A 卷（适中）解析

#### 一、单选题（30分）

1.  **答案：C**
    *   **解析：** 标识符由字母、数字、下划线组成，不能以数字开头，不能包含连字符（`-`）。A以数字开头，B是关键字，D包含连字符。C合法。
2.  **答案：B**
    *   **解析：** Python 3 中 `round(3.5)` 采用“银行家舍入法”（四舍六入五取偶），结果为 4；`int(3.9)` 是截断取整，结果为 3。
3.  **答案：C**
    *   **解析：** 字符串是不可变对象。`s.replace()` 会返回一个新的字符串对象，而**不会**修改原字符串 `s`。
4.  **答案：B**
    *   **解析：** 切片 `[start:end]` 是左闭右开区间。索引 1, 2, 3 对应的值分别是 2, 3, 4。
5.  **答案：B**
    *   **解析：** `random` 是随机数库。`math` 是数学库，`turtle` 是绘图库，`pandas` 是数据分析扩展库。
6.  **答案：C**
    *   **解析：** `dict.get(key, default)` 方法。如果键 `'c'` 不存在，则返回第二个参数（默认值）`0`。
7.  **答案：C**
    *   **解析：** 列表是可变对象，且 `b = a` 是引用赋值（贴标签），`a` 和 `b` 指向内存中同一个列表。修改 `b` 也会影响 `a`。
8.  **答案：A**
    *   **解析：** `jieba` 是最常用的 Python 中文分词库。
9.  **答案：C**
    *   **解析：** `'w'` 模式打开文件，如果文件已存在，会清空其内容重新写入；如果不存在则创建。
10. **答案：A**
    *   **解析：** `json` 是标准库，无需安装。`load` 用于文件流，`loads` 用于字符串。`json` 可以处理字典和列表。
11. **答案：A**
    *   **解析：** `*args` 用于接收任意数量的位置参数（打包成元组），`**kwargs` 用于接收关键字参数。
12. **答案：C**
    *   **解析：** 列表推导式生成列表。`range(3)` 是 0, 1, 2。平方后是 0, 1, 4。
13. **答案：A**
    *   **解析：** `matplotlib` 是 Python 的绘图/数据可视化标准库。
14. **答案：B**
    *   **解析：** 集合（Set）的特性是无序性、互异性（不重复）。
15. **答案：C**
    *   **解析：** `math.ceil()` 是向上取整函数，3.1 向上取整为 4。

#### 二、简答题（10分）

**参考答案：**
1.  **区别：**
    *   **可变性：** 列表（List）是**可变**的，可以进行增删改操作；元组（Tuple）是**不可变**的，一旦创建不能修改。
    *   **语法：** 列表使用方括号 `[]`，元组使用圆括号 `()`。
2.  **应用场景：**
    *   **列表：** 适用于存储需要频繁修改、排序或追加的数据集合，如“学生成绩列表”。
    *   **元组：** 适用于存储固定不变的数据，或作为字典的键（因为不可变），如“一周七天的名称”、“坐标点 (x, y)”。

#### 三、改错题（10分）

**题1：**
*   错误：`if x = 10:`
*   改正：`if x == 10:` （解析：条件判断应该用比较运算符 `==`，而不是赋值 `=`）

**题2：**
*   错误：`def init(self, name):`
*   改正：`def __init__(self, name):` （解析：构造函数前后各有两个下划线）

#### 四、编程题（50分）

**1. 基础运算（参考代码）：**
```python
sum_val = 0
for i in range(1, 101):
    # 能被3整除 且 不能被5整除
    if i % 3 == 0 and i % 5 != 0:
        sum_val += i
print(sum_val)
```

**2. 函数与随机数（参考代码）：**
```python
import random

def generate_code(n):
    code = ""
    for _ in range(n):
        # 生成A-Z的随机字符，A的ASCII是65，Z是90
        char = chr(random.randint(65, 90))
        code += char
    return code

# 测试
print(generate_code(4))
```

**3. 列表与字典处理（参考代码）：**
```python
students = [{"name": "Alice", "score": 85}, {"name": "Bob", "score": 72}, {"name": "Cindy", "score": 90}]

total_score = 0
max_score = -1
best_student = ""

for stu in students:
    # 累加总分
    total_score += stu['score']
    # 寻找最高分
    if stu['score'] > max_score:
        max_score = stu['score']
        best_student = stu['name']

avg_score = total_score / len(students)
print(f"平均分: {avg_score:.2f}")
print(f"最高分学生: {best_student}")
```

**4. 文件操作与CSV（参考代码）：**
```python
import csv

result_list = []

# 使用 with open 自动关闭文件
try:
    with open('data.csv', 'r') as f:
        # 使用 csv.DictReader 可以直接将每行读取为字典
        reader = csv.DictReader(f)
        for row in reader:
            result_list.append(dict(row))
    
    print(result_list)
except FileNotFoundError:
    print("文件 data.csv 未找到")
```

---

### 🔴 模拟试题 B 卷（较难）解析

#### 一、单选题（30分）

1.  **答案：C**
    *   **解析：** A: `not True` 为 False; B: `True and False` 为 False; C: `'a'` 在 `'apple'` 中，为 True; D: 空列表为 False。
2.  **答案：B**
    *   **解析：** 字符串切片 `[::-1]` 表示倒序翻转。
3.  **答案：A**
    *   **解析：** Python 对小整数（-5 到 256）有缓存机制（Small Integer Caching），所以两个 `10` 的 `id` 是一样的。
4.  **答案：C**
    *   **解析：** `lambda` 关键字用于定义匿名函数。
5.  **答案：D**
    *   **解析：** `append`, `sort`, `reverse` 都是列表的原地方法（In-place），会修改原列表。`sorted(lst)` 是内置函数，返回一个新列表，**不修改**原列表。
6.  **答案：B**
    *   **解析：** `pickle` 模块涉及二进制序列化，必须使用二进制写入模式 `'wb'`。
7.  **答案：C**
    *   **解析：** `__name__` 属性在直接运行脚本时值为 `'__main__'`，被导入时值为模块名。这用于控制代码块仅在直接运行时执行。
8.  **答案：B**
    *   **解析：** `&` 是集合的交集运算。A 和 B 的公共元素是 3。
9.  **答案：B**
    *   **解析：** `a` 接收 1，`b` 接收 3（覆盖默认值），`*args` 接收剩余的位置参数 `(4, 5)`，形式为元组。
10. **答案：B**
    *   **解析：** `numpy` 是用于科学计算和矩阵运算的核心库。
11. **答案：D**
    *   **解析：** Python 没有真正的私有属性（Private）。双下划线开头的属性（如 `__attr`）只是触发了**名称改写（Name Mangling）**，变成了 `_ClassName__attr`，在类外部依然可以通过这个改写后的名字访问，并非完全无法访问。
12. **答案：B**
    *   **解析：** `map` 对每个元素乘 2。结果是 `[2, 4, 6]`。
13. **答案：B**
    *   **解析：** `math.floor` 是向下取整（往数轴左边取）。-3.5 向下取整是 -4。
14. **答案：C**
    *   **解析：** 字典推导式 `{x: x**2}`。2->4, 4->16, 6->36。结果是字典 `{2:4, 4:16, 6:36}`。
15. **答案：B**
    *   **解析：** `csv.reader` 默认将每行数据读取为一个字符串列表。A 错误，可以不写表头；C 错误，CSV 是文本格式；D 错误，可以用任何文本编辑器打开。

#### 二、简答题（10分）

**参考答案：**
1.  **导入机制：** Python 导入模块时，会按照 `sys.path`（包含当前目录、环境变量、标准库路径等）的顺序查找。找到后会执行模块内的代码，并将模块对象加载到内存中。如果再次导入，通常直接使用内存中的缓存，不会重新执行。
2.  **`if __name__ == '__main__':` 的作用：**
    *   **作用：** 判断当前模块是作为主程序直接运行，还是被作为模块导入到其他文件中。
    *   **场景：** 用于编写测试代码。当直接运行该文件时，执行测试代码；当该文件被其他模块导入时（如 `import my_module`），这部分代码不会执行，避免副作用。

#### 三、改错题（10分）

**题1：**
*   错误1：`for` 循环末尾缺少冒号。
*   错误2：`Integer(i)` 不是 Python 内置函数。
*   **改正：**
    ```python
    lst = ['1', '2', '3']
    new_lst = []
    for i in lst:          # 加上冒号
        new_lst.append(int(i))  # 使用 int()
    print(new_lst)
    ```

**题2：**
*   错误：`f.write(12345)`。写入文本文件时，参数必须是字符串。
*   **改正：**
    ```python
    f = open('test.txt', 'w')
    f.write(str(12345))  # 转换为字符串
    # 或者 f.write("12345")
    f.close()
    ```

#### 四、编程题（50分）

**1. 逻辑与算法（参考代码）：**
```python
import math

def is_prime(n):
    if n <= 1:
        return False
    # 优化算法：只需判断到 sqrt(n)
    for i in range(2, int(math.sqrt(n)) + 1):
        if n % i == 0:
            return False
    return True

primes = []
for i in range(1, 101):
    if is_prime(i):
        primes.append(i)

print(primes)
```

**2. 字符串与统计（参考代码）：**
```python
text = "Python is good. Python is simple."

# 1. 预处理：去除标点（简单处理），转小写
text = text.replace('.', '').lower()

# 2. 分割单词
words = text.split()

# 3. 统计词频
word_counts = {}
for word in words:
    word_counts[word] = word_counts.get(word, 0) + 1

# 4. 排序并输出前3
# 将字典项转换为元组列表，按值（次数）降序排序
sorted_words = sorted(word_counts.items(), key=lambda x: x[1], reverse=True)

for i in range(min(3, len(sorted_words))):
    print(f"{sorted_words[i][0]}: {sorted_words[i][1]}")
```

**3. 面向对象编程（参考代码）：**
```python
class BankAccount:
    def __init__(self, account_number):
        self.account_number = account_number
        self.balance = 0  # 初始余额为0

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f"存入 {amount} 成功，当前余额: {self.balance}")
        else:
            print("存款金额必须大于0")

    def withdraw(self, amount):
        if amount > self.balance:
            print("余额不足")
            return False
        else:
            self.balance -= amount
            print(f"取出 {amount} 成功，当前余额: {self.balance}")
            return True

    def get_balance(self):
        return self.balance

# 演示
account = BankAccount("NO.888888")
account.deposit(1000)
account.withdraw(500)
account.withdraw(600) # 应该失败
```

**4. 综合文件处理（参考代码）：**
```python
import json

# 假设 numbers.txt 存在，可以先创建一个用于测试
# with open('numbers.txt', 'w') as f:
#     f.write("10\n20\n30\n")

numbers = []
try:
    # 1. 读取文件
    with open('numbers.txt', 'r') as f:
        for line in f:
            # 去除换行符并转换类型
            line = line.strip()
            if line: # 确保不是空行
                numbers.append(int(line))
    
    if numbers:
        # 2. 计算统计量
        total_sum = sum(numbers)
        average = total_sum / len(numbers)
        
        result = {
            "sum": total_sum,
            "average": average
        }
        
        # 3. 写入 JSON
        with open('result.json', 'w') as f:
            json.dump(result, f)
            
        print("计算完成，结果已写入 result.json")
    else:
        print("文件为空")

except FileNotFoundError:
    print("未找到 numbers.txt 文件")
except ValueError:
    print("文件包含非数字内容")
```