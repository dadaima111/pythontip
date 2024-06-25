# PythonTip 150

### 1.编写一个程序将分钟转换为秒。

- 定义函数`convert_to_seconds()`，参数为`minutes`。

- 在函数内，将分钟转换为秒（**1分钟=60秒**），并返回结果。

  ```python
  def convert_to_seconds(minutes):
      seconds = minutes * 60
      return seconds
  # 输入分钟
  input_minutes = int(input())
  # 调用函数 
  print(convert_to_seconds(input_minutes))
  ```

### 2.编写一个程序将字符串转换为整数。

- 定义函数`convert_to_int()`，参数为`str_number`。
- 在函数内，将字符串参数转换为整数并返回。

```python
def convert_to_int(str_number):
    int_number = int(str_number)
    return int_number
# 获取字符串输入
input_string = input()
result = convert_to_int(input_string)
# 打印结果的类型
print(type(result))
```

### 3.编写一个程序，找出列表中最大和最小数字之间的差值。

- 定义函数`difference_max_min()`，参数为`list_nums`。

- 在函数内部，找出列表中的最大和最小数字，并返回差值。

  ```python
  def difference_max_min(list_nums):
      # 在此处编写代码
      a = max(list_nums) - min(list_nums)
      return a
  # 输入整数，并将其转换为列表
  numbers = list(map(int, input().split()))  # map(int, input().split())表示按照整数排列
  
  # 调用函数
  print(difference_max_min(numbers))
  ```

### 4.编写一个程序，返回**整数**列表中的最后一个元素。

- 定义函数`last_element()`的函数，参数为列表`my_list`。
- 在函数中，返回列表的最后一一个元素。

```python
def last_element(my_list):
    end_list = my_list.pop()
    return end_list
# 获取整数输入，并将其转换为列表
input_list = list(map(int, input().split()))
# 调用函数
print(last_element(input_list))
```

### 5.编写一个程序来检查两个字符串是否具有相同数量的字符。

- 定义函数`compare_length()`，有两个参数`str1`和`str2`。

- 在函数内，如果`str1`的长度等于`str2`的长度，则返回`True`，否则返回`False`。

  ```python
  def compare_length(str1, str2):
      if len(str1) == len(str2):
          return True
      else:
          return False
  # 获取输入 
  input_str1 = input()
  input_str2 = input()
  
  # 调用函数 
  print(compare_length(input_str1, input_str2))
  ```

### 6.编写一个程序来连接字符串的首尾字符。

- 定义函数`join_first_last()`，参数为`input_str`。

- 在函数内部，返回字符串的首尾字符的连接字符串。

  ```python
  def join_first_last(input_str):
      last_str = input_str[-1]
      first_str = input_str[0]
      return first_str + last_str
  # 输入字符串
  given_string = input()
  
  # 调用函数
  print(join_first_last(given_string))
  ```

### 7.编写一个程序来判断一个单词是否为复数。

- 定义函数`is_plural()`，参数为`term`(输入的单词)。

- 在函数内，如果单词以`s`结尾，则返回`True`，否则返回`False`。

  ```python
  def is_plural(term):
      term = list(term)
      if term.pop() == 's':
          return True
      else:
          return False 
  
  # 获取输入 
  input_word = input()
  
  # 调用函数并输出结果 
  print(is_plural(input_word))
  ```

### 8.编写一个程序，用于在一组整数中找出唯一的数字。假设列表中只有一个唯一的数字。

- 定义函数`find_unique_number()`，参数为`num_list`，数字列表。

- 在函数内部，找出只出现一次的数字，并返回它。

- 如果列表只有一个数字，则返回该数字。

- 如果列表为空，则返回`None`。

- 如果不存在这样的数字，则返回`None`。

  ```python
  def find_unique_number(num_list):
      if len(num_list) == 1:
          return num_list[0]
      elif len(num_list) == 0:
          return None
      else:
          for i in num_list:
              if num_list.count(i) == 1:
                  return i
  # 将输入的整数转换为列表
  numbers = list(map(int, input().split()))
  
  # 调用函数
  print(find_unique_number(numbers))
  ```

### 9.编写一个程序，创建一个给定范围内的整数列表。

- 定义函数`list_between()`，有两个参数`start`和`end`。

- 在函数内，创建一个介于`start`（不包括）和`end`（不包括）之间的所有整数的列表，并返回该列表。

  ```python
  def list_between(start, end):
      list = []
      for i in range(start+1, end):
          list.append(i)
      return list        
  # 获取输入的start 及 end
  start = int(input())
  end = int(input())
  
  # 调用函数
  print(list_between(start, end))
  ```
  

### 10.编写一个程序来判断一个数字是否为素数。

- 定义函数`check_prime()`，参数为一个数字。

- 在函数内，如果数字为素数，返回`True`，否则返回`False`。

  ```python
  def check_prime(num):
      if num == 2:
          return True
      for i in range(2, int(num)):
          if num % i == 0:
              return False
      return True
  
  # 输入一个整数
  number = int(input())
  
  # 调用函数
  print(check_prime(number))
  ```


### 11.编写一个Python程序来计算字符串中元音字母的数量。

- 定义函数`vowel_count()`，参数为`string`(表示字符串)。

- 在函数中统计字符串中的元音字母数，并返回计数。

  ```python
  def vowel_count(string):
      count = 0
      for i in string:
          if i == 'a' or i == 'e' or i == 'i' or i == 'o' or i == 'u':
              count += 1
      return count
  
  # 获取输入字符串 
  input_string = input()
  # 调用函数 
  print(vowel_count(input_string))
  ```

### 12.编写一个程序来求一个给定数字的所有因数。

- 定义函数`find_all_factors()`，参数为`num`。

- 在函数内部，返回一个列表，列表中的数字是输入数字`num`的所以因数。

- 如果输入数字小于**1**，则返回一个空列表。

  ```python
  def find_all_factors(num):
      list = []
      for i in range(1 , num + 1):
          if num % i == 0:
              list.append(i)
      return list
  
  # 输入一个数字 
  num = int(input())
  
  # 调用函数 
  print(find_all_factors(num))
  ```

### 13.编写一个程序，返回一个数字的数字列表，但需要以相反的顺序排列。

- 定义函数`reverse_number_digits()`，参数为一个数字`num`。

- 在函数内，将数字`num`转换为其相反顺序的数字列表。

  ```python
  def reverse_number_digits(num):
      num_list = list(map(int, str(num)))
      reverse_list = num_list[::-1]
      return reverse_list   
  
  # 获取用户输入
  num = int(input())
  
  # 调用函数
  print(reverse_number_digits(num))
  ```

### 14.编写一个Python程序来判断两个给定的字符串是否是错位词。

如果两个字符串具有相同的字符，但顺序不同，则被认为是彼此的错位词。 例如，`restful`和`fluster`是错位词。

- 定义函数`are_anagrams()`，有两个参数：`string1`和`string2`。

- 在函数内，如果两个字符串是错位词，则返回`True`，否则返回`False`。

  ```python
  def are_anagrams(string1, string2):
      str1 = string1.replace(" ","")
      str2 = string2.replace(" ","")
      list1 = list(str1.lower())
      list2 = list(str2.lower())
      if sorted(list1) == sorted(list2):
          return True
      else:
          return False
  
  # 获取输入string1 和 string2 
  string1 = input()
  string2 = input()
  # 调用函数并打印结果 
  print(are_anagrams(string1, string2))
  ```

### 15.编写一个Python程序来确定字符串中的所有字符是否相同。

- 定义函数`is_string_identical()`，参数为`text_string`(字符串)。

- 在函数内，如果字符串中的所有字符都相同，则返回`True`，否则返回`False`。

  ```python
  def is_string_identical(text_string):
      a = len(text_string)
      for i in text_string:
          if text_string.count(i) == a:
              return True
          else:
              return False
  
  # 获取输入 
  text_string = input()
  # 调用函数 
  print(is_string_identical(text_string))
  ```

### 16.编写一个Python程序，用于确定一个数字列表的乘积是否可以被该列表的和整除。

- 定义函数`is_product_divisible_by_sum()`的函数，该函数接受一个整数列表作为参数。

- 在函数内，如果列表中所有数字的乘积可以被该列表的和整除，则返回`True`，否则返回`False`。

  ```python
  def is_product_divisible_by_sum(numbers_list):
      sm = sum(numbers_list)
      cj = 1
      for i in numbers_list:
          cj = cj * i
          if sm % cj == 0:
              return True
          else:
              return False 
  
  # 获取整数输入并将其转换为列表
  numbers_list = list(map(int, input().split()))
  # 调用函数打印结果
  print(is_product_divisible_by_sum(numbers_list))
  ```

### 17.编写一个Python程序，找出列表中第**n**小的整数。

- 定义函数`find_nth_smallest()`，该函数接受整数列表`numbers_list`和整数`n`作为参数。

- 在函数内部，返回列表中第`n`小的整数。

- 如果`n`大于列表的长度，则返回`None`。

  ```python
  def find_nth_smallest(numbers_list, n):
      sorted_list = sorted(numbers_list)
      if n > len(numbers_list):
          return None
      else:
          return sorted_list[n - 1]
  
  # 将输入的整数转换为列表
  numbers_list = list(map(int, input().split()))
  # 获取n的输入
  n = int(input())
  # 调用函数
  print(find_nth_smallest(numbers_list, n))
  ```

### 18.编写一个函数，用于求两个整数的最大公约数（GCD）。

- 定义函数`find_gcd()`，有两个数字参数`a`和`b`。

- 在函数内部，返回`a`和`b`的最大公约数。

  ```python
  def find_gcd(a, b):
      if a % b == 0 or b % a == 0:
          return min(a, b)
      else:
          return 1
  
  # 输入整数
  first_number = int(input())
  second_number = int(input())
  # 调用函数
  print(find_gcd(first_number, second_number))
  ```

### 19.编写一个程序来检查一个字符串是否以另一个字符串结尾。

- 定义函数`ends_with()`，有两个参数`string1`和`string2`。

- 在函数内，如果`string1`以`string2`结尾，则返回`True`，否则返回`False`。

  ```python
  def ends_with(string1, string2):
      if string1.endswith(string2):   # str.endswith(suffix[, start[, end]])。   
          return True					# suffix -- 该参数可以是一个字符串或者是一个元素。
      else:							# start -- 字符串中的开始位置。
          return False				# end -- 字符中结束位置。
  
  # 获取输入字符串
  string1 = input()
  string2 = input()
  # 调用函数
  print(ends_with(string1, string2))
  ```

### 20.编写一个程序来计算字符串中所有数字的乘积。

- 定义函数`multiply_numbers_in_string()`，参数为`num_string`。

- 在函数内部，返回字符串中所有数字的乘积。

  ```python
  def multiply_numbers_in_string(num_string):
      # 将字符串输入转换为列表
      num_list = list(map(int, num_string.split()))
      a = 1
      for i in num_list:
          a = a * i
      return a
  ```

### 21.编写一个程序来检查一个单词是否为同源词。 **同源词**是指不包含任何重复字母的单词，例如`brown`，`fox`，`quick`等。

- 定义函数`is_string_isogram()`，参数为一个单词`word`。

- 在函数内，如果单词是同源词，则返回`True`，否则返回`False`。

  ```python
  def is_string_isogram(word):
      # 将单词转换为小写
      word = word.lower()
      for i in word:
          if word.count(i) != 1:
              return False
      return True
  
  # 从用户处获取输入
  word = input()
  # 调用函数
  print(is_string_isogram(word))
  ```

### 22.编写一个程序来计算整数的二进制表示中1的个数。

- 定义函数`count_binary_ones()`，参数为数字`num`。

- 在函数内，将数字转换为其二进制表示，并计算“1”的个数。

  ```python
  def count_binary_ones(num):
      a = bin(num)
      count_1 = a.count("1")
      return count_1
  
  # 从标准输入读取一个整数
  num = int(input())
  # 调用函数
  print(count_binary_ones(num))
  ```

### 23.编写一个程序来计算第n个四面体数。

- 定义函数`calc_tetrahedral_number()`，参数第n个数`n`。

- 在函数内，使用公式`(n*(n+1)*(n+2))/6)`计算第**n**个四面体数，并返回它。

  ```python
  def calc_tetrahedral_number(n):
      Tn = int((n * (n + 1) * (n + 2)) / 6)
      return Tn
      
  # 输入整数
  num = int(input())
  # 调用函数
  print(calc_tetrahedral_number(num))
  ```

### 24.编写一个程序，求出给定数字区间内的所有偶数。

- 定义函数`find_even_numbers()`，参数为`num`。

- 在函数内部，使用列表推导式从**1**到`num`查找所有偶数，并返回该列表。

- 如果`num <= 1`，则返回空列表`[]`。

  ```python
  def find_even_numbers(num):
      list = []
      for i in range(1, num + 1):
          if i % 2 == 0: 
              list.append(i)
      return list
  
  # 获取整数输入
  num = int(input())
  # 调用函数
  print(find_even_numbers(num))
  ```

### 25.编写一个程序来求出前**n**个奇数。

- 定义函数`find_first_n_odds()`，参数为`n`。

- 在函数内部，返回前`n`个奇数的列表。

  ```python
  def find_first_n_odds(n):
      list = []
      for i in range(1, n * 2):
          if i % 2 == 1:
              list.append(i)
      return list  
  
  # 获取输入n
  n = int(input())
  # 调用函数
  print(find_first_n_odds(n))
  ```

### 26.编写一个程序来生成第n个斐波那契数。

- 定义函数`fibonacci_number()`，参数为`n`。

- 在函数中返回第n个斐波那契数。

  ```python
  def fibonacci_number(n):
      if n <= 0:
          return 0
      elif n == 1:
          return 1
      else:
          return fibonacci_number(n - 1) + fibonacci_number(n - 2)
  
  # 输入n的整数
  n = int(input())
  # 调用函数
  print(fibonacci_number(n))
  ```

### 27.编写一个程序来翻转给定句子中的单词顺序。

- 定义函数`reverse_sentence_words()`，该函数接受一个参数`sentence`(表示句子)。

- 该函数应该返回翻转其单词顺序的句子。

- 考虑任何由空格字符分隔的序列作为一个单词。

- 不要在句子的开头或结尾添加额外的空格。

  ```python
  def reverse_sentence_words(sentence):
      list = sentence.split()
      list.reverse()
      my_string = ' '.join(list)
      return my_string
  # 获取输入
  sentence = input()
  # 调用函数并打印结果
  print(reverse_sentence_words(sentence))
  ```

### 28.编写一个程序，分别按字母顺序返回字典的键和值。

- 定义函数`get_sorted_keys_values()`，参数为`dict_obj`(字典类型)。

- 在函数内部，返回一个由两个列表组成的列表：一个列表是按字母顺序排列的字典键，另一个列表是它们对应的值。

  ```python
  def get_sorted_keys_values(dict_obj):
      key_list = []
      vlause_list = []
      for key in sorted(dict_obj.keys()):
          key_list.append(key)
      for key in key_list:
          vlause_list.append(dict_obj[key])
      return [key_list,vlause_list]
  ```
  

### 29.编写一个程序来计算一个单词中的音节数。

- 定义函数`count_syllables()`的函数，该函数接受一个参数`word`。

- 在函数内，计算`word`中的音节数并返回它。

  ```python
  def count_syllables(word):
      count = word.count('-')
      return count + 1
  
  # 获取用户输入
  word = input()
  # 调用函数
  print(count_syllables(word))
  ```

### 30.编写一个程序，将数字以千位分隔符的形式格式化。

- 定义函数`add_commas()`，该函数接受一个非负整数。

- 在函数内部，将数字转换为字符串，并将逗号`,`作为千位分隔符添加。

- 返回格式化后的字符串。

  ```python
  def add_commas(number):
      return format(number,',')
  
  # 获取用户输入
  number = int(input())
  # 调用函数
  print(add_commas(number))
  ```

### 31.编写一个程序，找出能被从1到给定数字n（包括n）的所有数字整除的最小正数(即最小公倍数)。

- 定义函数`smallest_multiple()`的函数，参数为`n`。

- 在函数内，返回能被从**1**到给定数字`n`（包括n）的所有数字整除而无余数的最小正数。

  ```python
  def smallest_multiple(n):
      if n==1 or n==2:
          return n
      a = 2
      for j in range(3, n+1):
          b = j
          num = a * b
          tmp = num / gcd(a, b)
          a = tmp
      return int(tmp) 
  def gcd(a, b):
      while a % b != 0:
          c = a % b
          a = b
          b = c
      return b
  # 输入n
  n = int(input())
  # 调用函数
  print(smallest_multiple(n))
  ```

### 32.编写一个程序，使用递归查找给定列表中的最大整数。

- 定义函数`find_highest_number()`，参数为列表`numbers_list`。

- 在函数内部，实现一个递归算法，找出列表中的最大数字，并返回它。

  ```python
  def find_highest_number(numbers_list):
      if len(numbers_list) == 1:
          return numbers_list[0]
      else:
          max_num = find_highest_number(numbers_list[1:])
          return max(max_num,numbers_list[0])
  
  # 输入数字并转为列表
  numbers_list = list(map(int, input().split()))
  
  # 调用函数打印结果
  print(find_highest_number(numbers_list))
  ```

### 33.编写一个程序，求出一个列表中偶数和奇数的和。

- 定义函数`calculate_sum()`，参数为一个数字列表`numbers_list`。

- 分别求出偶数和奇数的和。

- 最后，返回一个列表，第一个元素为偶数的和，第二个元素为奇数的和。

  ```python
  def calculate_sum(numbers_list):
      even_list = []
      odd_list = []
      for i in numbers_list:
          if i % 2 == 0:
              even_list.append(i)
          else:
              odd_list.append(i)
      return [sum(even_list),sum(odd_list)]
  
  # 获取输入转为列表
  numbers_list = list(map(int,input().split()))
  
  # 打印偶数和奇数的和
  print(calculate_sum(numbers_list))
  ```

### 34.编写一个程序，将两个数字字符串相加，并将其和作为字符串返回。

- 定义函数`add_numbers()`，它接受两个参数（字符串数字）。

- 在函数内，检查参数是否为空字符串或`None`。如果是，则返回`Invalid Operation`。

- 否则，将两个数字相加，并将和作为字符串返回。

  ```python
  def add_numbers(num1, num2):
      if num1 == "None" or num1 == "" or num2 == "None" or num2 == "":
          return "Invalid Operation"
      else:
          return str(int(num1) + int(num2))
  
  # 获取用户输入num1 和 num2 
  num1 = input()
  num2 = input()
  
  # 调用函数
  result = add_numbers(num1, num2)
  
  # 打印和
  print(result)
  ```

### 35.编写一个程序，将一个两位十六进制数转换为其等价的二进制。

- 定义函数`hex_to_binary()`，该函数接受单个参数`hex_number`（以`0xXX`格式表示的十六进制数）。

- 在函数内，将十六进制数转换为二进制，并将结果作为字符串返回。

  ```python
  def hex_to_binary(hex_number):
       b = bin(hex_number)[2:].zfill(8)
       str_b = b
       return str_b
   
  # 获取用户输入的16进制数
  hex_number = int(input(), 16)
  
  # 打印转换后的二进制数 
  print(hex_to_binary(hex_number))
  ```

### 36.编写一个程序来判断一个数字是否为**Harshad**数。

- 定义函数`is_harshad()`，参数为`num`（整数）。

- 在函数内，判断该数字是否为**Harshad**数，如果是，返回`True`，否则返回`False`。

  ```python
  def is_harshad(num):
      a = num // 100
      b = (num - (a * 100)) // 10
      c = num % 10
      if num % (a + b + c) == 0:
          return True
      else:
          return False
  # 获取用户输入
  num = int(input())
  
  # 显示输出
  print(is_harshad(num))
  ```

### 37.编写一个程序来判断一个句子是否为标题文本。

- 定义函数`is_title()`，参数为一个句子。

- 在函数内，如果句子中的每个单词都以大写字母开头，则返回`True`，否则返回`False`

  ```python
  def is_title(sentence):
      if sentence == sentence.title():
          return True
      else:
          return False
  
  # 从用户处获取输入
  input_sentence = input()
  # 调用函数
  print(is_title(input_sentence))
  ```

### 38.编写一个程序来查找列表中不重复的数字。

- 定义函数`find_unique()`，它接受一个列表作为参数。

- 在函数内部，找出列表中只出现一次的数字。

- 以列表中的出现的顺序返回唯一的数字

  ```python
  def find_unique(lst):
      list = []
      for i in lst:
          if lst.count(i) == 1:
              list.append(i)
      return list 
  
  # 获取用户输入并转为数字列表
  numbers = list(map(int, input().split()))
  
  # 调用函数
  print(find_unique(numbers))
  ```

### 39.编写一个程序来检查一个数字是否是双基回文数。

- 定义函数`check_double_base_palindrome()`，参数为整数。

- 在函数内，检查数字的十进制和二进制形式是否都是回文。

- 如果是双基回文，返回`True`，否则返回`False`。

  ```python
  def check_double_base_palindrome(number):
      #将整数转换成二进制数的字符串，并去掉前缀0b
      binStr = bin(number)[2:]
      #十进制数的字符串
      deciStr = str(number)
      binFlag = True
      #判断二进制是否是回文数
      i = 0   
      while i <= int(len(binStr) / 2) - 1:
          if (binStr[i] == binStr[-1 - i]):
              i += 1
          else:
              binFlag = False
              break;
      deciFlag = True
  # 判断十进制是否是回文数
      i = 0
      while i <= int(len(deciStr) / 2) - 1:
          if (deciStr[i] == deciStr[-1 - i]):
              i += 1
          else:
              deciFlag = False
              break;
      if binFlag and deciFlag:
          return True
      else:
          return False
  # 获取用户输入
  number = int(input())
  
  # 调用函数
  print(check_double_base_palindrome(number))
  ```

### 40.编写一个程序，查找给定列表中给定元素的所有索引。

- 定义函数`find_indices()`，它接受两个参数，一个`my_list`列表和一个`element`的变量。

- 该函数应返回`my_list`中出现`element`的所有索引的列表。

  ```python
  def find_indices(my_list, element):
      list = []
      for i in range(0, len(my_list)):
          if my_list[i] == element:
              list.append(i)
      return list
  
  # split()函数将输入的字符串分割成一个列表
  user_input = input().split()
  element = input()
  
  # 调用函数 
  print(find_indices(user_input, element))
  ```


### 41.编写一个程序来计算两个给定单词之间相同字符的数量。

- 定义函数`shared_chars_count()`，有两个参数:`word1`和`word2`。

- 该函数应返回两个单词中相同字母的数量。

  ```python
  def shared_chars_count(word1, word2):
      my_list = []
      count = 0
      for i in word1:
          for j in word2:
              if i == j and (i not in my_list):
                  my_list.append(i)
                  count += 1 
      return count
  # 获取输入
  word1 = input()
  word2 = input()
  
  # 调用函数
  print(shared_chars_count(word1, word2))
  ```

### 42.编写一个程序来提取嵌套元组中的唯一元素。

- 定义函数`get_unique_elements()`，函数接受一个参数 - 一个包含三个元组的嵌套元组。

- 在函数内，提取所有元组中的独立元素，确保不重复提取元素。

- 以列表的形式返回唯一的元素，并**从小到大**排序。

  ```python
  def get_unique_elements(nested_tuples):
      list = []
      for i in nested_tuples:
          for j in i:
              if not j in list:
                  list.append(j)
      list.sort()
      return list
  
  # 初始化嵌套元组
  nested_tuples = []
  
  # 获取用户输入
  for _ in range(3):
      tuple_elements = tuple(map(int, input().split()))
      nested_tuples.append(tuple_elements)
  
  # 调用函数
  print(get_unique_elements(nested_tuples))
  ```

### 43.编写一个程序，计算两个日期之间的天数。

- 导入`datetime`模块。

- 定义函数`calculate_days_between()`数，其中有两个参数：`(date1, date2)`，类型为字符串，格式为`YYYY-MM-DD`。

- 在函数内，将字符串转换为`datetime`对象，并计算`date2`和`date1`之间的差异，以天为单位。

- 以天数的差异作为输出返回。

  ```python
  import datetime
  
  def calculate_days_between(date1, date2):
      datetime1 = datetime.datetime.strptime(date1,"%Y-%m-%d")
      datetime2 = datetime.datetime.strptime(date2,"%Y-%m-%d")
      if datetime1 < datetime2:
          res = (datetime2 - datetime1).days
      else:
          res = -(datetime1 - datetime2).days
      return res
  
  # 获取用户输入
  date1 = input()
  date2 = input()
  
  # 调用函数
  print(calculate_days_between(date1, date2))
  ```

### 44.编写一个程序，将给定单词的每个字母替换为字母表中的下一个字符。

- 定义函数`shift_char()`，接受一个参数`word`。

- 在函数内，将单词的每个字母替换为字母表中的下一个字母。

- 最后，返回转换后的单词。

  ```python
  def shift_char(word):
      my_string = " "
      for i in word:
          if i == " ":
              my_string += i        
          else:
              my_string += chr(ord(i)+1)  # 转换成ASCII值
      return my_string
  
  
  # 获取单词
  word = input()
  # 调用函数 
  print(shift_char(word))
  ```

### 45.编写一个程序，计算给定列表中缺失数字的总和。

- 定义函数`sum_missing_numbers()`，参数为`nums`（一个整数列表）。

- 在函数内，计算`nums`列表中的最小值和最大值。

- 计算最小值和最大值之间缺失的数字的总和。

- 返回缺失数字的总和。

  ```python
  def sum_missing_numbers(nums):
      nums.sort()
      nums_sum = ((nums[0] + nums[-1]) * (nums[-1] - nums[0] + 1)) / 2
      for i in nums:
          nums_sum -= i
      return int(nums_sum)
  
  # 获取输入转为数字列表 
  nums = list(map(int, input().split()))
  
  # 调用函数 
  print(sum_missing_numbers(nums))
  ```

### 46.编写一个程序将字典转换为列表，列表的每一个元素表示一个键值对，并按键排序。

- 定义函数`dict_to_sorted_list()`，其参数为`dictionary`。

- 在函数中，将字典转换为列表，其中每个列表的元素包含**键**及其相应的**值**。

- 按升序对此列表排序。

- 返回排序后的列表。

  ```python
  def dict_to_sorted_list(dictionary):
      my_list = []
      for keys, values in dictionary.items():
          dictlist = []
          dictlist.append(keys)
          dictlist.append(values)
          my_list.append(dictlist)
      my_list.sort()
      return my_list 
  
  # 获取输入转为字典
  dictionary = eval(input())
  
  # 调用函数 
  print(dict_to_sorted_list(dictionary))
  ```

### 47.编写一个程序，返回一个按字母顺序排序的字符串，其中包含给定字符串中不出现的所有小写字母。

- 定义函数`get_missing_letters()`，参数为`word_string`。

- 在函数内部，返回一个排序的字符串，其中包含不出现在`word_string`中的所以小写字母。

  ```python
  def get_missing_letters(word_string):
      my_string = " "
      for i in range(ord('a'),ord('z')+1):
          if chr(i) not in word_string:
              my_string += chr(i)
      return my_string
  # 获取输入的字符串 
  word_string = input()
  
  # 调用函数输出结果 
  print(get_missing_letters(word_string))
  ```

### 48.编写一个程序来计算列表中子列表的数量。

- 定义函数`count_sublists()`，参数为`list_input`。

- 在函数内部，返回输入列表中子列表的总数。

  ```python
  def count_sublists(list_input):
      if list_input is None:
          return 0
      elif isinstance(list_input[0],list):  # isinstance用来判断一个对象是否是一个已知的类型
          return len(list_input)
      else:
          return 0
  
  # 获取输入转为列表 
  list_input = eval(input())
  
  # 调用函数 
  print(count_sublists(list_input))
  ```

### 49.编写一个程序来计算字符串中重复出现多次的不同字符的数量。

- 定义函数`count_duplicate_chars()`，参数为`input_string`。

- 在函数内部，计算并返回字符串中重复字符的数量。

  ```python
  def count_duplicate_chars(input_string):
      list = []
      for i in input_string:
          if input_string.count(i) > 1 and i not in list:
              list.append(i)
      return len(list)
  
  # 获取用户输入
  test_string = input()
  
  # 调用函数
  result = count_duplicate_chars(test_string)
  print(result)
  ```

### 50.编写一个程序，计算句子中每个单词中某个字符出现的次数。

- 定义函数`count_char_occurrences()`，有两个参数:`sentence`(句子)和`char`(字符)。

- 在函数内部，将`sentence`转换为小写。

- 返回一个列表，包含`char`在句子的每个单词中出现的次数。

  ```python
  def count_char_occurrences(sentence, char):
      my_list = sentence.lower().split()
      list = []
      for word in my_list:
          list.append(word.count(char))
      return list
      
      
  # 获取输入 
  sentence_input = input()
  char_input = input()
  
  # 调用函数 
  print(count_char_occurrences(sentence_input, char_input))
  ```

### 51.编写一个程序，在单词中的每个大写字母前添加空格，然后将字符串中的每个字符转换为小写。

- 定义函数`add_space_before_capital()`，它接受一个参数`word`。

- 在函数中，在字符串的每个大写字母前添加空格，并转为小写字符串后返回。

  ```python
  def add_space_before_capital(word):
      my_string = ""
      for i in range(0,len(word)):
          if word[i] >= 'A' and word[i] <= 'Z':
              my_string += " "
              my_string += word[i]
          else:
              my_string += word[i]
      return my_string.lower()
  
  # 获取用户输入
  word = input()
  
  # 调用函数
  print(add_space_before_capital(word))
  ```

### 52.编写一个程序，找出一个句子中最长的单词。如果有两个或多个单词长度相同，返回第一个最长的单词。

- 定义函数`get_longest_word()`，它接受一个参数：`sentence`。

- 在函数内部，实现识别最长单词的逻辑，并返回第一个最长单词。

  ```python
  def get_longest_word(sentence):
      my_list = sentence.split()
      list = []
      for word in my_list:
          list.append(len(word))
          max_word = max(list)
      index = list.index(max_word)
      return my_list[index]
  # 获取输入 
  sentence = input()
  
  # 调用函数 
  print(get_longest_word(sentence))
  ```
  

### 53.编写一个程序来检查一个整数是否是完美数。

- 定义函数`check_perfect()`，参数为`num`。

- 在函数内，如果数字`num`是完美数，返回`True`，否则返回`False`。

  ```python
  def check_perfect(num):
      count = 0
      for i in range(1, num):
          if num % i == 0:
              count += i
      if count == num:
          return True
      else:
          return False
  # 输入处理 
  num = int(input())
  
  # 调用函数 
  print(check_perfect(num))
  ```
  

### 54.编写一个程序，用于判断给定字符串中字母在字母表中的位置和是否为偶数。

- 定义函数`is_sum_even()`，参数为`string`。

- 在函数内，计算`string`中字母在字母表中的位置和（不区分大小写）。

- 忽略字符串中的非字母符号。

- 如果和为偶数，则返回`True`，否则返回`False`。

  ```python
  def is_sum_even(string):
      my_list = string.split()
      count = 0
      for word in my_list:
          for i in word:
              count += ord(i) - 96
      if count % 2 == 0:
          return True
      else:
          return False
  
  # 获取字符串 
  string = input()
  
  # 调用函数 
  print(is_sum_even(string))
  ```

### 55.编写一个程序，将8位二进制数转换为其十进制等效值。

- 定义函数`binary_to_decimal()`，它接受一个单独的列表参数`binary_list`。

- 在函数内部实现从二进制到十进制的转换逻辑。

- 返回二进制数的十进制等效值。

  ```python
  def binary_to_decimal(binary_list):
       my_string = ""
       for word in binary_list:
            my_string += str(word)
       return int(my_string, 2)
  
  # 获取输入，并转为列表 
  binary_list = list(map(int, input().split()))
  
  # 调用函数 
  print(binary_to_decimal(binary_list))
  ```

### 56.编写一个程序来查找列表中最大的偶数。如果列表中没有偶数，则返回`-1`。

- 定义一个名为`find_largest_even()`的函数，该函数接受一个列表作为参数。

- 在函数内部，遍历列表并找到最大的偶数。

- 如果没有找到偶数，则返回`-1`。

  ```python
  def find_largest_even(lst):
      list = []
      for i in lst:
          if i % 2 == 0:
              list.append(i)
      if list == []:
          return -1
      else:
          return max(list)
  
  # 获取输入转为整数列表 
  input_list = list(map(int, input().split()))
  
  # 调用函数 
  print(find_largest_even(input_list))
  ```

### 57.编写一个程序，判断一个列表中的数字是否可以重新排列成一个连续的数字序列。

- 定义函数`is_consecutive_sequence()`，参数为`num_list`。

- 在函数内，对列表进行排序。

- 然后，检查排序后的列表是否形成一个连续的序列，即每两个相邻元素之间的差值是**1**。

- 如果序列是连续的，则返回`True`，否则返回`False`。

  ```python
  def is_consecutive_sequence(num_list):
      num_list.sort()
      for i in range(1, len(num_list)):
          if num_list[i] - num_list[i-1] != 1:
              return False
      else:
          return True
  
  # 获取输入转为整数列表 
  nums = list(map(int, input().split()))
  
  # 调用函数 
  print(is_consecutive_sequence(nums))
  ```
  

### 58.编写一个程序，输入一个正整数，将其转换为二进制，然后反转二进制字符串，最后返回反转后的二进制字符串对应的十进制数。

- 定义函数`reverse_binary_integer()`，参数为一个整数。

- 在函数内，将整数转换为二进制表示，反转二进制字符串，然后将其转换回十进制。

- 返回最后的十进制数。

  ```python
  def reverse_binary_integer(n):
      bin_2 = bin(n)[2:]
      my_string = bin_2[::-1]
      int_10 = int(my_string, 2)
      return int_10
  # 获取输入 
  n = int(input())
  
  # 调用函数 
  print(reverse_binary_integer(n))
  ```

### 59.编写一个程序来计算给定单词中辅音字母和元音字母的数量。

- 定义函数`count_consonants()`，参数为`word`。该函数应返回单词中辅音字母的数量。

- 定义函数`count_vowels()`，参数为`word`。该函数应返回单词中元音字母的数量。

  ```python
  def count_consonants(word):
      count = 0
      for i in word:
          if i.lower() >= 'a' and i.lower() <= 'z' and i not in ['a','e','i','o','u']:
              count += 1
      return count
  def count_vowels(word):
      count = 0
      for i in word:
          if i.lower() >= 'a' and i.lower() <= 'z' and i in ['a', 'e', 'i', 'o', 'u']:
              count += 1
      return count
  
  # 获取用户输入
  word = input()
  
  # 调用函数
  print(count_consonants(word))
  print(count_vowels(word))
  ```

### 60.编写一个程序，将每个单词的最后一个字母大写。

- 定义函数`capitalize_last_letter()`，参数为`sentence`(字符串)。

- 该函数应返回每个单词最后一个字母大写的字符串。

  ```python
  def capitalize_last_letter(sentence):
      reverse_sentence = sentence[::-1].title()
      return reverse_sentence[::-1]
  
  # 获取输入 
  sentence = input()
  
  # 调用函数 
  print(capitalize_last_letter(sentence))
  ```

### 61.编写一个程序来查找两个列表中的相同元素。

- 定义函数`find_common_elements()`，它接受两个整数列表参数，`list1`和`list2`。

- 在函数内部，找到共同的数字，并按升序返回它们。

  ```python
  def find_common_elements(list1, list2):
       list = []
       for i in list1:
            for j in list2:
                 if i == j:
                      list.append(i)
       return list
  
  # 获取用户输入，转换为列表
  list1 = list(map(int, input().split()))
  list2 = list(map(int, input().split()))
  
  # 调用函数
  print(find_common_elements(list1, list2))
  ```

### 62.编写一个程序，检查给定日期是否为**dd/mm/yyyy**和**mm/dd/yyyy**格式的回文日期。

- 定义函数`is_date_palindromic()`，接受一个参数`date_in_string`（以**dd/mm/yyyy**格式的日期字符串）。

- 如果给定的日期在**dd/mm/yyyy**和**mm/dd/yyyy**格式下都是回文日期，函数应该返回`True`，否则返回`False`。

  ```python
  def is_date_palindromic(date_in_string):
      my_string = date_in_string.replace("/", "")
      if my_string[::] == my_string[::-1] and my_string[0:1] == my_string[2:3]:
          return True
      else:
          return False
  
  # 获取日期输入 
  date_in_string = input()
  
  # 调用函数 
  print(is_date_palindromic(date_in_string))
  ```

### 63.编写程序确定一个已排序整数列表的最大间隔。

- 定义函数`max_gap()`，参数为整数列表`lst`。

- 在函数内，对列表进行排序，然后找出两个连续元素之间的最大差值。

- 返回最大差值。

  ```python
  def max_gap(lst):
      lst.sort()
      list = []
      for i in range(0, len(lst)-1):
          list.append(lst[i + 1] - lst[i])
      return max(list) 
  
  # 获取用户输入，转换为整数列表
  numbers = list(map(int, input().split()))
  # 调用函数，输出结果
  print(max_gap(numbers))
  ```

### 64.编写一个程序找出两个单词之间的共同字母。

- 定义函数`common_letters()`，它接受两个参数:`word1`和`word2`。

- 该函数应返回一个包含`word1`和`word2`之间均出现的字母的组成的字符串。

- 返回的字符串中的字母应为小写并按字母顺序排序。

- 如果没有相同的字母，则返回一个空字符串。

  ```python
  def common_letters(word1, word2):
      my_list = []
      for i in word1:
          for j in word2:
              if i == j and i not in my_list:
                  my_list.append(i)
      my_list.sort()
      my_string = ''.join(my_list)
      return my_string
  
  # 输入两个单词
  word1 = input()
  word2 = input()
  
  # 调用函数, 并打印结果
  print(common_letters(word1, word2))
  ```

### 65.编写一个程序，将两个列表合并，并按照第一个列表的顺序对合并后的列表进行排序。

- 定义一个名为`merge_and_sort()`的函数，其中有两个列表参数，`first_list`和`second_list`。

- 在函数内部，合并两个列表。

- 检查第一个列表是升序还是降序排列。

- 按照第一个列表的顺序对合并后的列表进行排序。

- 返回排序后的列表。

  ```python
  def merge_and_sort(first_list, second_list):
      my_list = first_list + second_list
      if first_list[0] >= first_list[-1]:  # 判断是否降序
          my_list.sort(reverse=True)
          return my_list
      else:
          my_list.sort()
          return my_list
  
  
  # 获取输入，转换为列表
  first_list = list(map(int, input().split()))
  second_list = list(map(int, input().split()))
  
  # 调用函数
  print(merge_and_sort(first_list, second_list))
  ```

### 66.编写一个程序递归判断一个字符串是否为回文。

- 定义函数`is_string_palindrome()`，参数为`string`。

- 在函数内部，实现递归，如果字符串是回文，则返回`True`，否则返回`False`。

  ```python
  def is_string_palindrome(string):
      if len(string) < 2:
          return True
      elif string[0] != string[-1]:
          return False
      else:
          return is_string_palindrome(string[1:-1]) 
  
  # 获取用户输入
  user_input = input()
  
  # 调用函数
  print(is_string_palindrome(user_input.lower()))
  ```

### 67.编写一个程序将表示二进制数字的元组转换为整数。

- 定义函数`binary_to_int()`，它接受一个参数`bin_tuple`。

- 在函数内，将二进制元组转换为十进制整数，并返回结果。

  ```python
  def binary_to_int(bin_tuple):
      my_list = list(bin_tuple)
      my_string = ''.join(map(str,my_list))
      return int(my_string, 2)
  
  # 读取输入，将输入转换为元组 
  bin_tuple = tuple(map(int,input().strip().split()))
  
  # 调用函数binary_to_int()，并输出结果
  print(binary_to_int(bin_tuple))
  ```

### 68.编写一个程序，求一个正整数数组中每对相邻元素的最大值。

- 定义函数`max_adjacent()`，接收一个正整数列表为输入。

- 在函数内部，创建一个新的列表，其中的每个元素都是输入数组中每对相邻元素的最大值。

- 返回这个新列表。

  ```python
  def max_adjacent(arr):
      my_list = []
      for i in range(0,len(arr)-1):
          if arr[i+1] > arr[i]:
              my_list.append(arr[i+1])
          else:
              my_list.append(arr[i])
      return my_list
  
  # 获取输入，转换为列表 
  arr = list(map(int, input().split()))
  
  # 调用函数，输出结果 
  result = max_adjacent(arr)
  print(result)
  ```

### 69.编写一个程序，检查列表是否存在两数字之和等于给定的数。

- 定义函数`is_sum_present()`，它接受两个参数 - 一个数字列表`num_list`和一个数字`target_sum`。

- 在函数内，检查列表中的每对数字。如果任意一对数字的和等于`target_sum`，则返回`True`。否则，返回`False`。

  ```python
  def is_sum_present(num_list, target_sum):
      for i in range(0, len(num_list)):
          for j in range(i+1,len(num_list)):
              if num_list[i] + num_list[j] == target_sum:
                  return  True
      return False
  
  # 获取输入
  num_list = list(map(int, input().split()))
  target_sum = int(input())
  
  # 调用函数 
  print(is_sum_present(num_list, target_sum))
  ```

### 70.编写一个程序，计算列表中每个元素的出现的次数，并以字典返回。

- 定义函数`count_frequency()`，该函数接受一个元素列表`lst`作为参数。

- 在函数内部，返回一个字典，其中列表的元素作为键，其相应的次数作为值。

  ```python
  def count_frequency(lst):
      values = []
      keys = []
      for value in lst:
          values.append(value)
          keys.append(lst.count(value))
      return dict(zip(values,keys))		# 将两个列表合并成字典
  
  # 获取用户输入 
  lst = list(input().split())
  
  # 调用函数 
  print(count_frequency(lst))
  ```


### 71.编写一个程序，找出最小的N位数字，满足指定值的倍数。

- 定义函数`smallest_multiple()`，有两个参数，`digits`（即N）和`multiple_of`（整数）。

- 在函数内，返回最小的N位数数字，它是指定值的倍数。

  ```python
  def smallest_multiple(digits, multiple_of):
      min_num = pow(10, digits-1)
      max_num = pow(10, digits)
      for i in range(min_num,max_num):
          if i % multiple_of == 0:
              return i
  
  # 获取输入 
  digits = int(input())
  multiple_of = int(input())
  
  # 调用函数，输出结果 
  print(smallest_multiple(digits, multiple_of))
  ```

### 72.编写一个程序，按照每个单词的最后一个字母对句子进行排序。

- 定义函数`sort_by_last_char()`，参数为`sentence`(表示句子)。

- 在函数内部，返回按照每个单词最后一个字母排序的句子。

  ```python
  def sort_by_last_char(sentence):
       reverse_sentence = sentence[::-1]
       my_list = list(reverse_sentence.split())
       my_list.sort()
       my_reverse_list = []
       for word in my_list:
            my_reverse_list.append(word[::-1])
       my_reverse_string = ' '.join(my_reverse_list)
       return my_reverse_string
  # 输入句子 
  sentence = input()
  
  # 调用函数 
  print(sort_by_last_char(sentence))
  ```

### 73.编写一个程序，检查是否可以通过连接给定的较小列表来形成目标列表。

- 定义函数 `can_form_target()`，该函数有两个参数：`list_of_lists`（整数列表的列表）和 `target_list`（整数列表）。

- 在函数内部，将 `list_of_lists` 中的所有列表连接起来，并与 `target_list` 进行比较。如果它们相同（忽略顺序），则返回 `True`，否则返回 `False`。

  ```python
  def can_form_target(list_of_lists, target_list):
      linklist = []
      for list in list_of_lists:
          for i in list:
              linklist.append(i)
      linklist.sort()
      target_list.sort()
      if linklist == target_list:
          return True
      else:
          return False
  
  # 获取用户输入
  user_list_of_lists = [list(map(int, input().split())) for _ in range(int(input()))]
  user_target_list = list(map(int, input().split()))
  
  # 调用函数
  print(can_form_target(user_list_of_lists, user_target_list))
  ```

### 74.编写一个程序，根据给定位置的字符对单词进行排序。

- 定义函数`sort_words_by_char()`，它接受两个参数，一个`words`列表和一个`index`(位置)。

- 在函数内，根据每个单词中给定位置的字符对列表进行排序。按字母升序排列。

- 该函数应返回排序后的列表。

  ```python
  def sort_words_by_char(words, index):
      list1 = []
      list2 = []
      for word in words:
          if index > len(word):
              return False
          else:
              word = word[index-1] + word
              list1.append(word)
      list1.sort()
      for word in list1:
          list2.append(word[1:])
      return list2
  
  # 获取用户输入
  words = input().split() # 单词列表
  index = int(input())    # 位置
  
  # 调用函数
  print(sort_words_by_char(words, index))
  ```

### 75.编写一个程序将字符串转换为字典。

- 定义函数`convert_str_list_to_dict()`，参数为`str_list`(输入的字符串)。

- 在函数内部，创建一个字典，其中每个字符串使用`=`进行分割，第一部分为**键**，第二部分为**值**。

- 返回字典。

  ```python
  def convert_str_list_to_dict(str_list):
      dict = {}
      for str in str_list.split(" "):
          strlist = str.split("=")
          dict[strlist[0]] = strlist[1]
      return dict
  # 输入字符串 
  str_list = input()
  
  # 调用函数 
  print(convert_str_list_to_dict(str_list))
  ```

### 76.编写一个程序，计算从两个字符串中移除的最少字母数，使它们成为变位词。

- 定义函数 `min_removals_to_anagram()`，有两个参数：`str1` 和 `str2`。

- 在函数内，计算从两个字符串中移除的最小字母数，使它们成为变位词。

  ```python
  def min_removals_to_anagram(str1, str2):
      str1 = sorted(str1)
      str2 = sorted(str2)
      tmp = []
      i = 0
      while i < len(str1):
          j = 0
          while j < len(str2):
              if str1[i] == str2[j]:
                  tmp.append(str1[i])
                  tmp.append(str2[j])
                  break
              j += 1
          i += 1
      return len(str1) + len(str2) - len(tmp)
  # 获取输入 
  str1 = input()
  str2 = input()
  
  # 调用函数，输出结果 
  print(min_removals_to_anagram(str1, str2))
  ```

### 77.编写一个程序，创建一个字典，其中给定单词的每个唯一字母表示一个键，值为字母出现的索引的列表。

- 定义函数`letter_indices()`，参数为`word`(字符串)。

- 在函数中，创建一个字典，其中键是单词中的唯一字母，值是包含该字母出现的索引的列表。

- 返回该字典

  ```python
  def letter_indices(word):
      value = []
      dict = {}
      for i in range(0,len(word)):
          if word[i] not in dict:
              value.append(i)
              dict[word[i]] = value
              value = []
          else:
              tmplist = dict[word[i]]
              tmplist.append(i)
              dict[word[i]] = tmplist
      return dict
  
  # 获取输入 
  word = input()
  
  # 调用函数 
  print(letter_indices(word))
  ```
  

### 78.编写一个程序，确定给定字符串中子字符串的重复次数。

- 定义函数`repetitions_in_string()`，该函数接受一个字符串参数。

- 在函数中，返回提供的字符串中子字符串的重复次数。

  ```python
  def repetitions_in_string(s):
      my_string = ""
      for i in range(0,len(s)):
          my_string += s[i]
          for k in range(1,len(s)):
              if my_string * k == s:
                  return k
      return 1
  # 获取输入 
  test_string = input()
  
  # 调用函数 
  print(repetitions_in_string(test_string))
  ```

### 79.编写一个程序来交换字典的键和值。

- 定义函数`swap_dict()`，参数为一个字典`dict`。

- 在函数内部，反转给定字典的键和值。如果一个值出现多次，将对应键组合在一个列表中。

  ```python
  def swap_dict(dict):
      keyList = []
      valueList = []
      resDict = {}
      for key,value in dict.items():
          keyList.append(value)
          valueList.append(key)
      tmp = []
      for i in range(0,len(keyList)):
          if keyList[i] not in resDict:
              tmp = []
              tmp.append(valueList[i])
              resDict[keyList[i]] = tmp
          else:
              value = resDict[keyList[i]] + valueList[i].split()
              resDict[keyList[i]] = value
      return resDict
  # 读取输入的字典 
  dict = eval(input())
  
  # 调用函数 
  print(swap_dict(dict))
  ```

### 80.编写一个程序将字符串从**驼峰式**写法转换为**下划线写法**。

- 定义函数`convert_to_snake_case()`，接收一个字符串作为参数。

- 在函数内部，将字符串转换为**下划线写法**，并返回它。

  ```python
  def convert_to_snake_case(s):
     my_string = ""
     for i in range(0,len(s)):
        if s[i].islower():    # 判断是否全是小写字母
           my_string += s[i]
        else:
           my_string += "_"
           my_string += s[i].lower()
     return my_string
  
  # 获取输入 
  input_string = input()
  
  # 调用函数，打印输出 
  print(convert_to_snake_case(input_string))
  ```

### 81.编写一个程序来检查给定的数字是否可以表示为两个或多个连续正数的和。

- 定义函数`check_consecutive_sum()`，参数为`n`。

- 在函数内，检查该数字`n`是否可以表示为连续数字的和。

- 如果该数字可以表示为连续数字的和，则返回`True`，否则返回`False`。

  ```python
  def check_consecutive_sum(n):
      for i in range(1,n):
          tmp = i
          sum = 0
          while sum < n:
              sum += tmp
              tmp += 1
              if sum == n:
                  return True
              elif sum > n:
                  break
      return False
          
  
  # 获取输入数字n
  n = int(input())
  
  # 调用函数 
  print(check_consecutive_sum(n))
  ```

### 82.编写一个程序来确定给定字符串是否为异位词。

- 定义函数`is_heterogram()`，参数为字符串`s`。

- 在函数内，如果字符串是异位词，则返回`Yes`，否则返回`No`。

  ```python
  def is_heterogram(s):
      my_str = s.replace(" ","")
      for i in my_str:
          if my_str.count(i) > 1:
              return "No"
      return "Yes"
  # 获取输入 
  input_string = input()
  
  # 调用函数，输出结果 
  print(is_heterogram(input_string))
  ```

### 83.编写一个程序来检查给定的字符串是否为另一个字符串的子集。

- 定义函数`is_subset()`，有两个参数：`sub_string`和`main_string`(均是字符串)。

- 在函数内，如果`sub_string`是`main_string`的子集，则返回`True`，否则返回`False`。

  ```python
  def is_subset(sub_string, main_string):
      str = ""
      for i in sub_string:
          for j in main_string:
              if i == j :
                  str += i
      if sub_string == str:
          return True
      else:
          return False
  
  # 获取用户输入
  sub_string = input()
  main_string = input()
  
  # 调用函数
  print(is_subset(sub_string, main_string))
  ```

### 84.编写一个程序将嵌套列表扁平化为一维列表(即元素均不是列表)。

- 定义函数`flatten_list()`，该函数有一个参数`list_of_lists`。

- 在函数中，创建一个新的一维列表，其中包含子列表中的所有元素。

- 返回新创建的列表。

  ```python
  def flatten_list(list_of_lists):
      my_list = []
      for list in list_of_lists:
          for i in list:
              if i % 1 == 0:
                  my_list.append(i)
      return my_list
  
  # 初始化嵌套列表
  list_of_lists = []
  
  # 获取用户输入
  # 子列表的数量
  n = int(input())
  
  # 子列表
  for _ in range(n):
      sublist = list(map(int, input().split()))
      list_of_lists.append(sublist)
  
  # 调用函数
  print(flatten_list(list_of_lists))
  ```

### 85.编写一个程序来计算一个数字的阶乘，并计算该阶乘的各位数字之和。

- 定义函数`sum_of_digits_in_factorial()`的函数，参数为`num`。

- 在函数内，首先计算`num`的阶乘，然后返回阶乘中数字的和。

  ```python
  def sum_of_digits_in_factorial(num):
      count = 1
      sum = 0
      for i in range(1,num+1):
          count = count * i
      str_count = str(count)
      for i in str_count:
          sum += int(i)
      return sum
  # 获取用户输入
  num = int(input())
  
  # 调用函数
  print(sum_of_digits_in_factorial(num))
  ```

### 86.编写一个程序来确定给定数字的最大质因数。

- 定义函数`largest_prime_factor()`，它接受一个参数`num`。

- 在函数内部，计算并返回`num`的最大质因数。

  ```python
  def isPrime(num):
      if num == 2:
          return True
      for i in range(3,num):
          if num % i == 0 and num != i:
              return False
      return True
  def largest_prime_factor(num):
      numlist = []
      for i in range(2,num):
          if num % i == 0:
              num = int(num / i)
              numlist.append(i)
      i = 0
      max = 1
      while i < len(numlist):
          if isPrime(numlist[i]):
              max = numlist[i]
              i += 1
          else:
              i += 1
      return max
  
  
  # 获取输入数字
  user_input = int(input())
  
  # 调用函数 
  print(largest_prime_factor(user_input))
  ```

### 87.编写一个程序，根据某个条件过滤字典值。

- 定义函数`filter_dict_values()`，有两个参数：字典`mixed_dict`和整数`k`。

- 在函数内部，创建一个新字典，并从`mixed_dict`过滤值不是整数或大于整数`k`的键值对，然后存储到新字典中。

- 返回新字典。

  ```python
  def filter_dict_values(mixed_dict, k):
      my_dict = {}
      for key, value in mixed_dict.items():
          if type(value) != int:
              my_dict[key] = value
          elif int(value) > k:
              my_dict[key] = value
      return my_dict
  
  # 获取输入 
  user_dict = eval(input())
  user_k = int(input())
  
  # 调用函数 
  print(filter_dict_values(user_dict, user_k))
  ```
  

### 88.编写一个程序将一个集合转换为字典。

- 定义函数`convert_set_to_dict()`，接收一个参数`input_set`（一个整数集合）。

- 在函数内部，将集合转换为字典，将集合中的每个项作为键，并将值均设为**0**。

- 按键排序字典（升序）并返回排序后的字典。

  ```python
  def convert_set_to_dict(input_set):
      my_dict = {}
      new_input_sort = sorted(input_set)
      for set in new_input_sort:
          my_dict[set] = 0
      return my_dict 
  
  # 获取输入，转为集合
  input_set = set(map(int, input().split()))
  
  # 调用函数 
  print(convert_set_to_dict(input_set))
  ```

### 89.编写一个程序，使用提供的键列表从字典中删除指定的键集合。

- 定义函数`remove_keys()`，有两个参数：字典`dict_input`和键列表`key_list`。

- 在函数中，从字典中删除`key_list`中存在的所有键。

- 返回更新后的字典。

  ```python
  def remove_keys(dict_input, key_list):
      for word in key_list:
          dict_input.pop(word)
      return dict_input
  
  # 获取输入 
  user_dict = eval(input())
  user_key_list = input().split()
  
  # 调用函数 
  print(remove_keys(user_dict, user_key_list))
  ```

### 90.编写一个程序来验证一个邮箱地址是否合法。

- 定义函数`is_email_valid()`，参数为`email`。

- 在函数内，如果邮箱`email`满足下面提到的条件，则返回`True`，否则返回`False`。

  ```python
  def is_email_valid(email):
      flag1 = False
      flag2 = False
      list1 = []
      index1 = email.find(".")
      index2 = email.find("@")
      if index1 != -1 and index2 != -1:		# 查找不到返回-1
          flag1 = True
      for i in range(0,len(email)):
          if email[i] == ".":
              list1.append(i)
      if list1[len(list1)-1] > index2 and index2 > 1:
          flag2 = True
      if flag1 and flag2:
          return True
      else:
          return False
  # 获取输入 
  email = input()
  
  # 调用函数 
  print(is_email_valid(email))
  ```

### 91.编写一个Python程序，计算给定范围内的回文数的数量。

- 定义函数`count_palindromes()`的函数，有两个参数：`start_number`和`end_number`。

- 在函数中，返回回文数的总计数，即在`start_number`和`end_number`之间的回文数量。

  ```python
  def count_palindromes(start_number, end_number):
      count = 0
      for number in range(start_number,end_number+1):
          number = str(number)
          if number == number[::-1]:
              count += 1
      return count
  
  # 获取输入 
  start_number = int(input())
  end_number = int(input())
  # 调用函数 
  print(count_palindromes(start_number, end_number))
  ```

### 92.编写一个程序来检查是否可以重新排列给定的单词字母来形成回文单词。

- 定义函数`can_form_palindrome()`的函数，参数为`word`(即输入的单词)。
- 在函数内，如果输入字符串可以重新排列以形成回文，则返回`True`，否则返回`False`。

```python
def can_form_palindrome(word):
    countList = []
    word = sorted(word)
    i = 0
    while i < len(word):
        tmpCount = word.count(word[i])
        countList.append(tmpCount % 2)	# 找出奇数的字符个数是否超过1个，超过1个肯定不能排列成回文
        i += tmpCount
    if countList.count(1) > 1:
        return False
    return True   

# 从用户处获取输入
word = input()
# 调用函数
print(can_form_palindrome(word))
```

### 93.编写一个程序，将一个数字列表按照指定大小分割成特定大小的块。

- 定义函数`list_into_chunks()`的函数，有两个参数`num_list`和`chunk_size`。

- 在函数内，将`num_list`分割成大小为`chunk_size`的子列表。

- 将这些子列表作为列表返回。

  ```python
  import math
  def list_into_chunks(num_list, chunk_size):    
      resList = []
      #特殊场景，chunk_size=1
      if chunk_size == 1:
          for num in num_list:
              tmp = []
              tmp.append(num)
              resList.append(tmp)
          return resList
      #向上取整，以便获取到子列表的数目
      subListNum = math.ceil(len(num_list) / chunk_size)
      subList = []
      for i in range(0,len(num_list)):
      #场景1：假设chunk_size=4，那么取索引为0,4,8,12的元素做为子列表的第一个
          if i % chunk_size == 0:
              subList = []
              subList.append(num_list[i])
      #场景2：假设chunk_size=4，那么取索引为3,7,11,15的元素出来，因为是子列表的最后一个元素，所以该子列表要加到父列表中
          elif i % chunk_size == chunk_size-1:
              subList.append(num_list[i])
              resList.append(subList)
      #特殊情况：剩下的列表中的数全部取出来，加到resList列表的最后一个子列表里（假设原列表长13，假设chunk_size=4，那么还剩下了单独的一个元素）
              if len(resList) + 1 == subListNum:
                  resList.append(num_list[i+1:])
      #场景3：假设chunk_size=4，那么取索引为其他非场景1和场景2的元素出来，加入到子列表中
          else:
              subList.append(num_list[i])
      return resList
  # 从用户输入中获取数据，并将其转换为列表
  num_list = list(map(int, input().split()))
  # 从用户输入中获取块大小
  chunk_size = int(input())
  # 调用函数
  print(list_into_chunks(num_list, chunk_size))
  ```

### 94.编写一个程序，查找给定字母最近的元音。

- 定义函数`closest_vowel()`，参数为一个字母`letter`。

- 在函数内，确定给定字母最近的元音。

- 如果两个元音离给定字母距离相等，则返回字母顺序较小的元音。

  ```python
  def closest_vowel(letter):
      lower = letter.lower()
      vowel = ['a','e','i','o','u']
      if letter in vowel:
          return letter
      for i in range(0,len(vowel)):
          if i + 1 == len(vowel) and letter > 'u':
              return 'u'
          if vowel[i] < letter < vowel[i + 1]:
              len1 = ord(letter) - ord(vowel[i])
              len2 = ord(vowel[i+1]) - ord(letter)
              if len1 <= len2:
                  return vowel[i]
              else:
                  return vowel[i + 1]
  # 获取输入
  letter = input()
  # 调用函数
  print(closest_vowel(letter))
  ```


### 95.编写一个程序来统计缺失的数字并返回它们的总和。

- 定义函数`missing_numbers_info()`的函数，参数为`num_list`。

- 在函数中，返回一个元组，元组中有两个元素：缺失数字的数量和它们的总和。

- 如果没有缺失的数字，则返回**(0, 0)**。

  ```python
  def missing_numbers_info(num_list):
      min_num = min(num_list)
      max_num = max(num_list)
      list = []
      for i in range(min_num,max_num):
          if i not in num_list:
              list.append(i)
      tuple = (len(list),sum(list))
      return tuple
  # 获取整数输入并将其转换为列表
  num_list = list(map(int, input().split()))
  # 调用函数
  print(missing_numbers_info(num_list))
  ```

### 96.编写一个程序来找出句子中最长和最短的单词。不要忽略字母数字或空格字符。

- 定义函数`extreme_words_in_sentence()`的函数，参数为一个。

- 在函数内部，返回一个元组，元组中有两个元素：句子中最长的单词和最短的单词。

- 如果多个单词具有相同的长度，则返回第一个出现的。

  ```python
  def extreme_words_in_sentence(sentence):
      list = []
      wordlist = sentence.split(" ")
      for word in wordlist:
          list.append(len(word))
      maxword = wordlist[list.index(max(list))]
      minword = wordlist[list.index(min(list))]
      return (maxword.lower(),minword.lower())
  # 处获取输入
  sentence = input()
  # 调用函数
  print(extreme_words_in_sentence(sentence))
  ```
  

### 97.编写一个程序来找出给定数字的排列。

- 定义函数`get_all_permutations()`，该函数接受一个包含三个整数的列表作为参数。

- 在函数内部，找出所有可能的数字排列，并在新行中打印每个排列。

  ```python
  def get_all_permutations(digits):
      for i in digits:
          for j in digits:
              for k in digits:
                  if  i != j and j != k and i != k:
                      print(i, j, k)
  
  # 获取整数输入并将其转换为列表
  digits = list(map(int, input().split()))
  # 调用函数
  get_all_permutations(digits)
  ```

### 98.编写一个程序来检查两个数字是否为二进制异位词。

- 定义函数`is_binary_anagram()`，有两个参数`num1`和`num2`。

- 在函数内，将两个数字转换为其二进制表示，并检查它们是否为异位词。如果是，则返回`True`，否则返回`False`。

  ```python
  def binary_anagram(num1, num2):
      num1_bin = bin(num1)[2:]
      num2_bin = bin(num2)[2:]
      if num1_bin.count("1") ==num2_bin.count("1"):
          return True
      else:
          return False
  
  # 获取输入 
  num1 = int(input())
  num2 = int(input())
  
  # 调用函数 
  print(binary_anagram(num1, num2))
  ```

### 99.编写一个程序，从一个元组中提取最大和最小的K个元素。

- 定义函数`extract_max_min()`，有两个参数：`input_tuple`（一个整数元组）和`k`（要提取的数量）。

- 在函数内部，从`input_tuple`中找到`k`个最小和`k`个最大的元素。

- 返回一个包含提取元素的元组，其中前`k`个元素是最小的，后`k`个元素是最大的。

  ```python
  def extract_max_min(input_tuple, k):
      # 对输入元组进行排序
      sorted_tuple = sorted(input_tuple)
      res_tuple = ()
      if k > len(sorted_tuple):
          return 0
      else:
          for i in range(0, k):
              res_tuple += (sorted_tuple[i],)
          for i in range(-k, 0):
              res_tuple += (sorted_tuple[i],)
      return res_tuple
  
  # 获取整数输入并将其转换为元组
  input_tuple = tuple(map(int, input().split()))
  # 获取K的值
  k = int(input())
  # 调用函数
  print(extract_max_min(input_tuple, k))
  ```

### 100.编写一个程序，将一个物品列表分解成一个列表中的单个物品。

- 定义函数`break_down_list()`，参数为`items`。

- 在函数内，对列表中的每个物品，创建一个具有相同`type`但`quantity`为**1**的新字典。

- 返回新的字典列表。

  ```python
  def break_down_list(items):
      res_list = []
      for item in items:
          res_dict = {}
          quantitytmp = item.get('quantity')
          typetmp = item.get('type')
          if quantitytmp == 0:
              continue
          for i in range(0,quantitytmp):
              res_dict['type'] = typetmp
              res_dict['quantity'] = 1
              res_list.append(res_dict)
      return res_list
  # 获取物品列表 
  items = eval(input())
  # 调用函数，输出分解后的物品列表
  print(break_down_list(items))
  ```


### 101.编写一个程序，将整数列表的每个元素与字典的每个项映射，形成一个嵌套字典。

- 定义函数`map_list_dict()`，它有两个参数`input_dict`和`input_list`。

- 在函数内部，将列表的每个元素映射到字典的相应键值对

- 形成一个新的字典，列表元素作为键，嵌套字典（包含输入字典的单个键值对）作为值并打印。

  ```python
  import json
  
  def map_list_dict(input_dict, input_list):
      resdict = {}
      for item in input_list:
          tmpdict = {}
          oldkey = list(input_dict.keys())[input_list.index(item)]
          oldvalue = input_dict[oldkey]
          tmpdict[oldkey] = oldvalue
          resdict[item] = tmpdict
      return resdict
  # 获取输入字符串并将其解析为json
  input_dict = json.loads(input())
  # 获取整数输入并将其转换为列表
  input_list = list(map(int, input().split()))
  # 调用函数
  print(map_list_dict(input_dict, input_list))
  ```

### 102.编写一个程序来生成给定整数集合的大小为**n**的所有子集。

- 定义函数`generate_subsets()`，有两个参数`input_set`(整数集合)和`n`。

- 在函数内部，生成`input_set`的大小为`n`的所有子集，并以列表返回。

  ```python
  from itertools import combinations
  
  # 定义函数
  def generate_subsets(input_set, n):
      list = []
      for i in combinations(input_set, n):
          list.append(set(i))
      return list
  
  # 输入整数并将其转换为集合
  input_set = set(map(int, input().split()))
  # 输入子集大小
  n = int(input())
  print(generate_subsets(input_set, n))
  ```

### 103.编写一个程序来计算列表中两个或多个连续**1**的块数。

- 定义函数`count_consecutive_ones()`，参数为`input_list`。

- 在函数内，计算`input_list`中两个或多个连续**1**的块数，并返回该计数。

  ```python
  def count_consecutive_ones(input_list):
      count = 0
      indexlist = []
      for i in range(0,len(input_list)):
          if input_list[i] == 1:
              indexlist.append(i)
      if len(indexlist) < 2:
          return 0
      for j in range(1, len(indexlist)-1):
          if indexlist[j + 1] - indexlist[j] != 1 and indexlist[j] - indexlist[j - 1] == 1:
              count += 1
      return count + 1
  
  # 获取输入, 转换为列表 
  input_list = list(map(int, input().split()))
  # 调用函数
  print(count_consecutive_ones(input_list))
  ```

### 104.编写一个程序来查找嵌套列表中缺失的列表的长度。假设只有一个缺失的列表。

- 定义函数`length_of_missing_list()`，参数为`list_of_lists`(嵌套列表)。

- 在函数中，从`list_of_lists`中返回缺失列表的长度。

- 如果没有缺失的列表，则返回`None`。

  ```python
  def length_of_missing_list(list_of_lists):
      my_list = []
      for reslist in list_of_lists:
          my_list.append(len(reslist))
      for i in range(min(my_list),max(my_list)+1):
          if i not in my_list:
              return i
  
  # 从用户输入中获取list_of_lists
  list_of_lists = eval(input())
  # 调用函数
  print(length_of_missing_list(list_of_lists))
  ```

### 105.编写一个程序，重复长度较小的字符串，直到长度等于较长字符串的长度。假设两个输入字符串的长度不相等。

- 定义函数`repeat_till_equal_length()`的函数，有两个参数`string1`和`string2`。

- 在函数内，重复较短的字符串，直到它等于较长的字符串的长度。

  ```python
  def repeat_till_equal_length(string1, string2):
      if len(string1) < len(string2):
          shortstring = string1
          longstring = string2
      else:
          shortstring = string2
          longstring = string1
      lendiff = len(longstring) - len(shortstring)
      i = int(lendiff / len(shortstring))
      j = lendiff % len(shortstring)
      strnew = shortstring + shortstring * i + shortstring[0:j]
      return strnew
  # 输入两个字符串
  string1 = input()
  string2 = input()
  # 调用函数
  print(repeat_till_equal_length(string1, string2))
  ```

### 106.编写一个程序来找出列表中最小缺失的正整数。

- 定义函数`find_missing_integer()`的函数，参数为`number_list`。

- 在函数内，返回列表中最小的缺失**正整数**。

  ```python
  def find_missing_integer(number_list):
      my_list = []
      for i in range(min(number_list),max(number_list)+1):
          if i not in number_list and i > 0:
              my_list.append(i)
      return my_list[0] 
  
  # 输入一串数字，以空格分隔，转换为列表
  number_list = list(map(int, input().split()))
  # 调用函数
  print(find_missing_integer(number_list))
  ```

### 107.编写一个程序，检查句子中的任何单词是否包含重复字母。

- 定义函数`check_duplicate_letters()`，参数为`phrase`(字符串)。

- 在函数内，如果字符串`phrase`的任何单词包含重复字母，则返回`True`，否则返回`False`。

  ```python
  def check_duplicate_letters(phrase):
      wordlist = phrase.split(" ")
      for word in wordlist:
          if len(set(word)) != len(word):
              return True
      return False
  
  # 获取输入
  sentence = input()
  # 调用函数
  print(check_duplicate_letters(sentence))
  ```

### 108.编写一个程序，查找离给定整数最近的回文数。

- 定义函数`find_closest_palindrome()`，参数为`num`。

- 在函数内部，返回最近的回文数。如果有两个回文数的**绝对距离**相同，返回较小的数。

- 如果给定数字本身就是回文数，则返回该数字。

  ```python
  def is_palindrome(n):
      return str(n) == str(n)[::-1]
  
  # 定义函数
  def find_closest_palindrome(num):
      if is_palindrome(num):
          return num
      i = num
      j = num
      while(True):
          if not is_palindrome(i):
              i += 1
          else:
              break
      while(True):
          if not is_palindrome(j):
              j -= 1
          else:
              break
      if i - num >= num - j:
          return j
      else:
          return i
  
  # 从用户处获取输入
  num = int(input())
  # 调用函数
  print(find_closest_palindrome(num))
  ```

### 109.编写一个程序，执行包括加法`+`、减法`-`、乘法`*`和除法`//`在内的基本算术运算。

- 定义函数`perform_arithmetic_operation()`，参数为`operation_string`(字符串)。

- 在函数内，执行字符串中指定的算术运算，并将结果作为数字返回。

- 如果运算为除法，且第二个数为**0**，则返回**-1**。

  ```python
  def perform_arithmetic_operation(operation_string):
      strlist = operation_string.split(" ")
      num1 = int(strlist[0])
      num2 = int(strlist[2])
      if strlist[1] == '+':
          return num1 + num2
      elif strlist[1] == '-':
          return num1 - num2
      elif strlist[1] == '*':
          return num1 * num2
      elif strlist[1] == '//' and num2 != 0:
          return num1 // num2 
      else:
          return -1
  
  # 获取输入
  operation_string = input()
  # 调用函数
  print(perform_arithmetic_operation(operation_string))
  ```

### 110.编写一个程序，找出一个数字列表的最大公约数。

- 定义函数`find_gcd_of_numbers()` ，它接受一个参数 `numbers_list`(数字列表)。

- 在函数内部，计算并返回列表中数字的最大公约数。

  ```python
  def gcd(a, b):
      if b == 0:
          return a
      return gcd(b, a % b)
  
  def find_gcd_of_numbers(numbers_list):
      i = 0
      number = numbers_list[0]
      while i < len(numbers_list) - 1:
          number = gcd(number, numbers_list[i + 1])
          i += 1
      return number
  
  # 获取整数输入并转换为列表
  numbers_list = list(map(int, input().split()))
  # 调用函数
  print(find_gcd_of_numbers(numbers_list))
  ```

### 111.编写一个程序，找出列表中比它右边的所有数字都大的数字。

- 定义函数`larger_than_following()`，参数为`num_list`。

- 在函数中，从`num_list`中返回比它右边的所有数字都大的数字的列表。

- 如果没有这样的数字，则返回空列表`[]`。

  ```python
  def larger_than_following(num_list):
      min = num_list[-1]
      list = []
      for num in range(len(num_list) - 2, -1 ,-1):
          if num_list[num] > min:
              min = num_list[num]
              list.append(num_list[num])
      return list[::-1] 
  
  # 获取输入，并将其转换为列表
  num_list = list(map(int, input().split()))
  # 调用函数
  print(larger_than_following(num_list))
  ```

### 112.编写一个程序来验证一个整数列表是否是排序列表向右旋转后的列表。假设输入列表中包含不重复的元素。

- 定义函数`is_sorted_rotated()`，接收一个整数列表作为输入。

- 在函数内，检查列表是否是排序列表旋转的（向右）。如果是，返回`True`。否则，返回`False`。

  ```python
  def is_sorted_rotated(input_list):
      sort_list = sorted(input_list)
      if input_list == sort_list:
          return False
      len1 = len(sort_list)
      for i in range(1, len1):
          tmp_list = sort_list[-i:] + sort_list[:-i]
          if input_list == tmp_list:
              return True
      return False 
  
  # 获取输入，将输入转换成列表
  input_list = list(map(int,input().split()))
  # 调用函数
  print(is_sorted_rotated(input_list))
  ```

### 113.编写一个程序，检查一个列表是否是另一个列表的有序子列表。

- 定义函数 `is_ordered_sublist()`，它接受两个参数：`sublist` 和 `main_list`。

- 在函数内部，如果子列表的所有元素都能按照相同的顺序在 `main_list` 中找到，则返回 `True`，否则返回 `False`。

  ```python
  def is_ordered_sublist(sublist, main_list):
      list = []
      for i in main_list:
          for j in sublist:
              if i == j:
                  list.append(i)
      if list == sublist:
          return True
      else:
          return False
  
  
  # 将整数输入转换为主列表
  main_list = list(map(int, input( ).split()))
  # 将整数输入转换为子列表
  sublist = list(map(int, input().split()))
  # 调用函数
  print(is_ordered_sublist(sublist, main_list))
  ```

### 114.编写一个程序，将列表中每个数字**降序排列**形变成新的数字。

- 定义函数`reorder_list_digits()`，参数为`num_list`(元素保证为正整数)。

- 在函数内，返回一个新列表，其中每个整数的数字都按降序重新排列。

  ```python
  def reorder_list_digits(num_list):
      reslist = []
      for num in num_list:
          strmap = sorted(str(num),reverse=True)
          reslist.append(int("".join(strmap)))
      return reslist
  
  
  # 获取输入的数字并转换为列表
  num_list = list(map(int, input().split()))
  # 调用函数
  print(reorder_list_digits(num_list))
  ```

### 115.编写一个程序，判断两个给定的列表(数字)，合并后是否形成一个数字连续的序列。

- 定义函数`is_consecutive_sequence()`，该函数有两个参数：`list1`和`list2`。

- 在函数内部，如果合并的列表形成一个连续的序列，则返回`True`，否则返回`False`。

  ```python
  def is_consecutive_sequence(list1, list2):
      list1.extend(list2)
      list1.sort()
      for i in range(1,len(list1)):
          if list1[i] - list1[i-1] != 1:
              return False
      return True
  # 将整数输入转换为列表
  list1 = list(map(int, input().split()))
  list2 = list(map(int, input().split()))
  # 调用函数
  print(is_consecutive_sequence(list1, list2))
  ```

### 116.编写一个程序来确定给定列表是否为几乎有序列表。

- 定义函数`is_almost_sorted()`，参数为一个列表`lst`。

- 在函数内部，如果列表是几乎有序的，则返回`True`，否则返回`False`。

- 另外如果列表已经有序(已经升序或降序)，则返回**-1**。

  ```python
  def is_almost_sorted(lst):
      lst_new1 = sorted(lst, reverse=True)
      lst_new2 = sorted(lst)
      if lst_new1 == lst or lst_new2 == lst:
          return -1
      i = 0
      while i < len(lst):
          tmp = lst[i]
          lst.remove(lst[i])
          lst_new1 = sorted(lst, reverse=True)
          lst_new2 = sorted(lst)
          if lst_new1 == lst or lst_new2 == lst:
              return True
          else:
              lst.insert(i,tmp)
              i += 1
      return False 
  
  # 获取用户输入，并将其转换为列表
  user_list = list(map(int,input().split()))
  # 调用函数
  print(is_almost_sorted(user_list))
  ```

### 117.编写一个程序，将字符串中**前后连续相同**字符聚合在一起，返回一个字符串列表。

- 定义函数`split_string_into_clusters()`，参数为`input_str`(输入的字符串)。

- 在函数内部，返回一个字符串列表，其中每个字符串由原始输入字符串中的前后相同字符组成。

  ```python
  def split_string_into_clusters(input_str):
      my_list = []
      i = 0
      tmp = ""
      while i < len(input_str) - 1:
          # 前后两个连续直到遇到不同的才加入列表中
          if input_str[i + 1]  == input_str[i]:
              tmp += input_str[i]
          # 最后两个元素
          elif input_str[i + 1]  != input_str[i] and i == len(input_str) - 2:
              tmp += input_str[i]
              my_list.append(tmp)
              my_list.append(input_str[i+1])
          # 前后两个元素不同把前一个元素加入列表中并清空字符串
          else:
              tmp += input_str[i]
              my_list.append(tmp)
              tmp = ""
          i += 1
      return my_list
  
  # 获取用户输入
  input_string = input()
  # 调用函数，输出结果
  print(split_string_into_clusters(input_string))
  ```

### 118.编写一个程序，用列表中的下一个最大数字替换列表中的每个整数。

- 定义函数`replace_with_next_largest()`，该函数参数`num_list`(数字列表)。

- 在函数内，用列表中的**下一个最大数字**替换输入列表中的当前整数，并返回修改后的列表。

- 如果元素是列表中最大的，则将其替换为**-1**。

  ```python
  def replace_with_next_largest(num_list):
      num_list_sort = sorted(num_list)
      reslist = []
      for i in range(0, len(num_list)):
          index = num_list_sort.index(num_list[i])
          if index + 1 == len(num_list):
              reslist.append(-1)
          else:
              reslist.append(num_list_sort[index + 1])
      return reslist
  
  # 将输入的整数转换为列表
  num_list = list(map(int, input().split()))
  # 调用函数
  print(replace_with_next_largest(num_list))
  ```

### 119.编写一个程序，从给定的字符串中移除特定的子串。

- 定义函数`remove_substrings()`，有两个参数：`main_string`(字符串)和`sub_list`(需要替换的子串列表)。

- 在函数内，从`main_string`中移除`sub_list`中所有的子串，然后返回`main_string`。

  ```python
  def remove_substrings(main_string, sub_list):
      for list1 in sub_list:
          main_string = main_string.replace(list1,"")
      return main_string
  
  # 获取字符串
  main_string = input()
  # 获取要移除的子串列表
  sub_list = input().split()
  # 调用函数
  print(remove_substrings(main_string, sub_list))
  ```

### 120.编写一个程序，将列表中的每个奇数平方。

- 定义函数`square_odd_numbers()`，该函数参数`nums`(数字列表)。

- 在函数内部，将列表中的每个奇数变为其平方数并添加到新的列表，返回新列表。

  ```python
  def square_odd_numbers(nums):
      strlist = []
      for num in input_list:
          if num % 2 == 0: 
              continue
          else:
              strlist.append(int(num) ** 2)
      return strlist
  # 获取整数输入并将其转换为列表
  input_list = list(map(int, input().split()))
  # 调用函数
  print(square_odd_numbers(input_list))
  ```

### 121.编写一个程序，从给定的数字中移除K位数字，得到最小的可能数字。

- 定义函数`smallest_number()`，有两个参数：`number`和`k`。

- 在函数内，以尽可能小的方式从给定的数字中移除`k`位数字，形成一个最小数字

  ```python
  import itertools
  def smallest_number(number, k):
      numstr = str(number)
      reslist = []
      combinations = list(itertools.combinations(numstr,len(numstr) - k))
      for num in combinations:
          reslist.append(int("".join(num)))
      return min(reslist) 
  
  # 获取数字
  number = int(input())
  # 获取k值，从数字中移除k位数字
  k = int(input())
  # 调用函数，输出结果
  print(smallest_number(number, k))
  ```

### 122.编写一个Python程序，从字符串中删除包含给定列表中任何字符的单词。

- 定义函数`remove_words_with_chars()`，它将接受两个参数：`sentence`和`char_list`。

- 在函数内，从`sentence`中删除有`char_list`中任何字符的单词。

- 如果最后`sentence`没有剩余的单词，则返回**-1**。

  ```python
  def remove_words_with_chars(sentence, char_list):
      sentencelist = sentence.split(" ")
      reslist = []
      for word in sentencelist:
          i = 0
          flag = True
          while i < len(char_list):
              if char_list[i] in word:
                  flag = False
                  break
              else:
                  i += 1
          if flag:
              reslist.append(word)
      if len(reslist) == 0:
          return -1
      return " ".join(reslist)
  # 获取句子
  sentence = input()
  # 从输入中获取要删除的字符列表，以空格分隔
  char_list = input().split()
  # 调用函数，输出结果
  print(remove_words_with_chars(sentence, char_list))
  ```

### 123.编写一个程序，找出已知面积和高的直角三角形的另外两边(底边及斜边)。

- 定义函数`find_missing_sides()`，有两个参数：`area`(面积)和`height`(高)。

- 在函数内，计算另外两边(低边`base` 及 斜边`hypotenuse`)，并将结果作为列表返回。使用`area`来求出底边，使用毕达哥拉斯定理求出斜边。

- 该函数应返回两个元素`[base, hypotenuse]`的列表。

  ```python
  import math
  def find_missing_sides(area, height):
      import math
      my_list = []
      base = area * 2 / height
      my_list.append(base)
      hypotensuse = height ** 2 + base ** 2
      x = math.sqrt(hypotensuse)
      my_list.append(x)
      return my_list
  
  # 输入面积
  area = int(input())
  # 输入高
  height = int(input())
  # 调用函数
  print(find_missing_sides(area, height))
  ```

### 124.编写一个程序，按照整数的位数从高到低的顺序对列表进行排序。

- 定义函数`digit_sort()`，参数为列表`numbers`。

- 在函数中，按照数字的长度从高到低排序列表中的数字。

- 同时，按照升序排序具有相同位数的数字。

- 返回排序后的数字列表。

  ```python
  def digit_sort(numbers):
      lenlist = []
      numbers = list(map(str, numbers))
      for i in numbers:
          if len(i) not in lenlist:
              lenlist.append(len(i))
      lenlist.sort(reverse=True)
      reslist = []
      for lennum in lenlist:
          tmplist = []
          i = 0
          while i < len(numbers):
              if lennum == len(numbers[i]):
                  tmplist.append(numbers[i])
              tmplist.sort()
              i += 1
          reslist += tmplist
      return list(map(int, reslist))
  # 获取输入，并将其转换为列表
  numbers = list(map(int, input().split()))
  # 调用函数
  print(digit_sort(numbers))
  ```

### 125.编写一个程序来查找两个字符串之间的最长公共结尾。

- 定义函数`longest_common_ending()`，有两个字符串参数`string1`和`string2`。

- 在函数内部，找到两个字符串之间的最长公共结尾，并返回它。

- 如果没有公共结尾，则返回**-1**。

  ```python
  def longest_common_ending(string1, string2):
      i = len(string1)
      j = len(string2)
      str = ""
      if string1[i - 1] != string2[j - 1]:
          return -1
      while i > 0 and j > 0:
          if string1[i - 1] == string2[j - 1]:
              str += string1[i -1]
              i -= 1
              j -= 1
          else:
              break
      return str[::-1]
  
  # 获取两个字符串
  string1 = input()
  string2 = input()
  # 调用函数
  print(longest_common_ending(string1, string2))
  ```

### 126.编写一个程序来确定一个列表中的所有字符串是否可以仅使用最长字符串中的字符来构成。

- 定义函数`check_string_compatibility()`，该函数有一个字符串列表参数`strings_list`。

- 在函数内，如果列表中的所有字符串都可以使用最长字符串中的字符来构成，则返回`True`，否则返回`False`。

  ```python
  def check_string_compatibility(strings_list):
      max_string = strings_list[0]
      for num in strings_list:
          if len(num) > len(max_string):
              max_string = num
      for str in strings_list:
          for i in str:
              if i not in max_string:
                  return  False
      return  True
  
  # 获取输入的字符串列表 
  strings_list = input().split()
  # 调用函数
  print(check_string_compatibility(strings_list))
  ```

### 127.编写一个程序，确定字符串的某个变位词是否可以成为另一个字符串的子串。

- 定义函数`is_anagram_present()`，有两个参数`string1`和`string2`。

- 在函数内，确定`string1`的某个变位词是否是`string2`的子串。如果是，返回`True`，否则返回`False`。

  ```python
  def is_anagram_present(string1, string2):
      list1 = []
      list2 = []
      my_list = []
      for i in string1:
          list1.append(i)
      for i in string2:
          list2.append(i)
      for i in list1:
          if i in list2: 
              my_list.append(i)
      if my_list == list1:
          return  True
      else:
          return False
      
  
  # 获取string1和string2的输入
  string1 = input()
  string2 = input()
  # 调用函数
  print(is_anagram_present(string1, string2))
  ```

### 128.编写一个程序，用于删除句子中每个单词的最后一个元音。

- 定义函数`remove_final_vowel()`，参数为句子`sentence`。

- 在函数内，在句子`sentence`中删除每个单词的最后一个元音，并返回新句子。

  ```python
  def remove_final_vowel(sentence):
      mystr = "" 
      for word in sentence.split(" "):
          i = len(word) - 1
          while i >= 0:
              if word[i].lower() in ['a','e','i','o','u']:
                  newword = word.replace(word[i], "")
                  break
              i -= 1
          mystr = mystr + str(newword) + " "
      return mystr
  # 获取输入
  input_string = input()
  # 调用函数
  print(remove_final_vowel(input_string))
  ```

### 129.编写一个程序，找出一个包含整数(也是字符串，但数字组成)和字符串的列表中最多重复的元素。

- 定义函数`most_repeated_elements()`，参数为`elements_list`。

- 在函数内，计算列表中最多重复的元素，并将其返回到一个新列表中。

- 如果两个元素的出现次数相同，则将两个元素都添加到列表中(按顺序添加)并返回该列表。

  ```python
  def most_repeated_elements(elements_list):
      resList = []
      elementDict = {}
  # 步骤1：将元组以及对应的出现次数存到字典elementDict里
      for elements in elements_list:
          if elements not in elementDict:
              elementDict[elements] = 1
          else:
              elementDict[elements] += 1
  # 步骤2：字典按照降序进行排序
      elementDict = dict(sorted(elementDict.items(), key=lambda x: x[1], reverse=True))
  # 步骤3：将字典的键和值转换成键列表和值列表
      keys = list(elementDict.keys())
      values = list(elementDict.values())
  # 步骤4：针对值列表进行判断，找出最多重复的元素
      for i in range(0, len(values) - 1):
  # 如果第一个值大，就将第一个值对应的键加入到列表里返回
          if values[i] > values[i + 1] and keys[i] not in resList:
              resList.append(keys[i])
              break
  # 如果有重复的值，那么这两个值对应的键都要加入到列表（需要判断下resList列表里没有该元素才能加入）
          elif values[i] == values[i + 1] and keys[i] not in resList:
              resList.append(keys[i])
              resList.append(keys[i + 1])
      return resList
  # 输入一个字符串，将其拆分为列表
  elements_list = input().split()
  # 调用函数
  print(most_repeated_elements(elements_list))
  ```

### 130.编写一个程序，统计列表中以特定子串开头的字符串的频率。

- 定义函数`prefix_frequency()`，它有两个参数：一个列表`str_list`和前缀字符串`prefix`。

- 在函数内部，返回`str_list`中以`prefix`开头的字符串的数量。

  ```python
  def prefix_frequency(str_list, prefix):
      count = 0
      for word in str_list:
          if word.startswith(prefix):
              count += 1
      return count
  # 接收字符串输入并将其分割成列表
  str_list = input().split()
  # 接收前缀的字符串输入
  prefix = input()
  # 调用函数
  print(prefix_frequency(str_list, prefix))
  ```

### 131.编写一个程序，判断两个数是否为亲和数。

- 定义函数 `are_amicable_numbers()`，该函数接受两个数字作为参数。

- 如果给定的数字是亲和数对，则函数返回 `True`，否则返回 `False`。

  ```python
  def are_amicable_numbers(num1, num2):
      count1 = 0
      count2 = 0
      for i in range(1,num1):
          if num1 % i == 0:
              count1 += i
      for i in range(1,num2):
          if num2 % i == 0:
              count2 += i
      if count1 == num2 and count2 == num1:
          return  True
      else:
          return False
  
  # 从用户那里获取整数输入
  num1 = int(input())
  num2 = int(input())
  # 调用函数
  print(are_amicable_numbers(num1, num2))
  ```

### 132.编写一个程序，找出将二进制字符串转换为`01`交替二进制字符串所需的最少转换次数。

- 定义函数`min_swaps_binary()`，该函数接受一个二进制字符串作为参数。

- 在函数内计算将给定的二进制字符串变为为**0**和**1**交替出现的字符串所需的最少转换次数。

  ```python
  def min_swaps_binary(binary):
      count1 = 0
      count2 = 1
      count3 = 0
      count4 = 1
      if binary[0] == '0':
          for i in range(1,len(binary)):
              if i % 2 == 1 and binary[i] != '1':
                  count1 += 1
              elif i % 2 == 0 and binary[i] != '0':
                  count1 += 1
          for i in range(1,len(binary)):
              if i % 2 == 1 and binary[i] != '0':
                  count2 += 1
              elif i % 2 == 0 and binary[i] != '1':
                  count2 += 1
          return min(count1,count2)
      else:
          for i in range(1,len(binary)):
              if i % 2 == 1 and binary[i] != '0':
                  count3 += 1
              elif i % 2 == 0 and binary[i] != '1':
                  count3 += 1
          for i in range(1,len(binary)):
              if i % 2 == 1 and binary[i] != '1':
                  count4 += 1
              elif i % 2 == 0 and binary[i] != '0':
                  count4 += 1
          return min(count3,count4)
  # 输入二进制字符串
  binary = input()
  # 输出最少转换次数
  print(min_swaps_binary(binary))
  ```

### 133.编写一个程序，找出所有元素之和严格超过给定值的**最短连续子列表**的长度。

- 定义函数`shortest_sublist_exceeds_n()`，它接受两个参数 - 一个整数列表`lst`和一个整数`n`。

- 该函数应返和严格大于`n`的最短子列表的长度。

- 如果不存在这样的子列表，函数应返回 **-1**。

  ```python
  def shortest_sublist_exceeds_n(lst, n):
      reslist = []
      for i in range(0, len(lst)):
          sum = lst[i]
          if sum > n:
              return 1
          lsttmp = [lst[i]]
          for j in range(i + 1, len(lst)):
              sum += lst[j]
              lsttmp.append(lst[j])
              if sum > n:
                  reslist.append(lsttmp)
                  break
      if len(reslist) == 0:
          return -1
      min = len(reslist[0])
      for lstinlst in reslist:
          if min > len(lstinlst):
              min = len(lstinlst)
      return min 
  # 获取用户输入
  lst = list(map(int, input().split()))
  n = int(input())
  
  # 调用函数
  print(shortest_sublist_exceeds_n(lst, n))
  ```

### 134.编写一个程序，返回给定整数的质因数。

- 定义函数`get_prime_factors()`，该函数接受一个参数`num`（正整数）。

- 该函数应返回传入参数的质因数列表，且从小到大排序。

  ```python
  def get_prime_factors(num):
      if is_prime(num):
          nullist = []
          nullist.append(num)
          return nullist
      numlist = []
      while num != 1:
          for i in range(2,num+1):
              if is_prime(i) and num % i == 0:
                  numlist.append(i)
                  num = num // i
      numlist = list(set(numlist))
      numlist.sort()
      return numlist
  # 判断num是否为质数
  def is_prime(num):
      if num == 2:
          return True
      for i in range(2, num//2 + 1):
          if num % i == 0:
              return False
      return True
  
  # 获取输入 
  num = int(input())
  
  # 调用函数
  print(get_prime_factors(num))
  ```

### 135.编写一个程序，找出一个列表的最小子集数，使得没有子集包含重复元素。

- 定义函数`minimum_subset()`，有一个整数列表参数`arr`。

- 在函数内部，实现找到没有子集具有重复元素的最小子集数的逻辑。

  ```python
  def minimum_subset(arr):
      reslist = []
      for i in range(0,len(arr)):
          reslist.append([])
      for i in range(0,len(arr)):
          for j in reslist:
              if arr[i] not in j:
                  j.append(arr[i])
                  break
      count = 0
      for list in reslist:
          if len(list) != 0:
              count += 1
      return count
  
  # 获取输入
  n = input()
  arr = list(map(int, n.split()))
  
  # 调用函数
  print(minimum_subset(arr))
  ```

### 136.编写一个程序，找出一个小于指定数的质数，且该质数可以表示为最多连续质数的和。

- 定义函数`find_consecutive_prime_sum()`，它接受一个整数`limit`作为参数。

- 函数应返回小于`limit`的质数，该质数是最多连续质数的和。

  ```python
  def is_prime(n):
      if n < 2:
          return False
      for i in range(2, int(n ** 0.5) + 1):
          if n % i == 0:
              return False
      return True
  
  
  def find_consecutive_prime_sum(limit):
      # 在这里编写你的代码
      consec_prime = []
      for i in range(limit + 1):
          if is_prime(i):
              consec_prime.append(i)
  
      result = {}
      for j in range(len(consec_prime)):
          for i in range(len(consec_prime)):
              if (i + j) <= len(consec_prime):
                  if (sum(consec_prime[i:i + j])) < limit and is_prime(sum(consec_prime[i:i + j])):
                      result[j] = sum(consec_prime[i:i + j])
  
      a = max(result.keys())
      return result[a]
  
  
  # 获取用户输入
  limit = int(input())
  
  # 调用函数
  print(find_consecutive_prime_sum(limit))
  ```

### 137.编写一个程序，找出两个n位数乘积中的最大回文数。

- 定义函数`largest_palindrome_product`，该函数接受一个参数`n`。

- 在函数内部，返回两个n位数的最大回文乘积。

  ```python
  def largest_palindrome_product(n):
      resList = []
  # 步骤1：特殊场景，1位数最大回文数是9
      if n == 1:
          return 9
  # 步骤2：循环遍历n位数
      for i in range(pow(10, n - 1), pow(10, n)):
          for j in range(pow(10, n - 1), pow(10, n)):
              product = i * j
              if str(product) == str(product)[::-1]:
                  resList.append(product)
  # 步骤3：返回回文数列表中的最大值
      return max(resList)
  # 获取用户输入
  n = int(input())
  # 调用函数
  print(largest_palindrome_product(n))
  ```

### 138.编写一个程序，计算一个列表中三个数字的最大和最小乘积。

- 定义函数`max_product_of_three()`，该函数接受一个数字列表`numbers`作为其参数。

- 在函数内部，计算并返回列表中任意三个数字的最大乘积。

- 定义第二个函数`min_product_of_three()`，该函数也接受一个数字列表`numbers`作为其参数。

- 在这个函数内部，计算并返回列表中任意三个数字的最小乘积。

  ```python
  from itertools import combinations
  def max_product_of_three(numbers):
      tupleList = list(combinations(numbers, 3))
      max_product = tupleList[0][0] * tupleList[0][1] * tupleList[0][2]
      for num in tupleList:
          if num[0] * num[1] * num[2] > max_product:
              max_product = num[0] * num[1] * num[2]
      return max_product
  def min_product_of_three(numbers):
      tupleList = list(combinations(numbers, 3))
      min_product = tupleList[0][0] * tupleList[0][1] * tupleList[0][2]
      for num in tupleList:
          if num[0] * num[1] * num[2] < min_product:
              min_product = num[0] * num[1] * num[2]
      return min_product
  # 获取用户输入
  numbers = list(map(int, input().split()))
  
  # 调用函数
  print(max_product_of_three(numbers))
  print(min_product_of_three(numbers))
  ```

### 139.编写一个程序，计算给定周长的直角三角形的最大面积。

- 定义函数`max_area_right_triangle()`，该函数有一个的整数参数`perimeter`(表示周长)。

- 在函数内，生成所有可能表示给定周长的直角三角形的三元组（**a**，**b**，**c**）。

- 确定并返回所有直角三角形中的最大面积。

  ```python
  def max_area_right_triangle(perimeter):
      a = float(perimeter / (2 + 2 ** 0.5))
      b = a
      return a * b / 2 
  
  # 获取输入 转为整数
  perimeter = int(input())
  
  # 调用函数
  print(max_area_right_triangle(perimeter))
  ```

### 140.编写一个程序来创建一个字符串的镜像图像。

- 定义函数`mirror_image()`，它有一个参数`str`(字符串)。

- 在函数内部，如果字符串`str`无法形成镜像图像，返回`Not Possible`。

- 否则，返回镜像字符串。

  ```python
  def mirror_image(str):
      # 定义可以形成镜像的字符对
      mirrorable_chars = {'b': 'd', 'd': 'b', 'p': 'q', 'q': 'p', 'i': 'i', 'o': 'o', 'x': 'x', 'v': 'v', 'w': 'w', 'u': 'u', 'm': 'm'}
      # 步骤1：先将字符串进行反转
      reverseStr = str[::-1]
      resStr = ""
  # 步骤2：针对反转后的字符串进行判断，如果字符在mirrorable_chars的键中，就增加到resStr中
      for i in reverseStr:
          if i in mirrorable_chars.keys():
              resStr += mirrorable_chars[i]
  # 不在，就返回Not Possible
          else:
              return "Not Possible"
      return resStr
  
  # 获取用户输入
  str = input()
  
  # 调用函数
  print(mirror_image(str))
  ```

### 141.编写一个程序，验证给定的分数是否是**非平凡**的数字消除分数。

- 定义函数`is_nontrivial_digit_cancelling()`，带有两个参数`numerator`(分子)和`denominator`(分母)，且均为整数。

- 在函数内部，检查分数`numerator/denominator`是否是非平凡的数字消除分数。

- 如果分数是非平凡的数字消除分数，则返回`True`，否则返回`False`。

  ```python
  def is_nontrivial_digit_cancelling(numerator, denominator):
      numeratorStr = str(numerator)
      denominatorStr = str(denominator)
      for i in numeratorStr:
          for j in denominatorStr:
              if i == j:
  # 如果i==j且0被消除，说明是平凡的
                  if i == "0":
                      return False
  # 否则消除
                  else:
                      numeratorStr = numeratorStr.replace(i, "")
                      denominatorStr = denominatorStr.replace(j, "")
  # 分数的值小于1说明是非平凡的
      if float(int(numeratorStr) / int(denominatorStr)) < 1:
          return True
      else:
          return False
  # 获取用户输入
  numerator = int(input())
  denominator = int(input())
  
  # 调用函数
  print(is_nontrivial_digit_cancelling(numerator, denominator))
  ```

### 142.编写一个程序来生成两个列表的所有唯一组合。

- 定义函数`unique_combinations()`，它接受两个列表作为参数，`list_a`和`list_b`。

- 该函数返回由将第一个列表的每个元素与第二个列表的元素配对形成的唯一组合的列表。

  ```python
  def unique_combinations(list_a, list_b):
      resList = []
  # 进行两轮循环
      for a in list_a:
  # 进入循环时将a列表元素加入到tmp列表
          list_tmp = [a]
          for b in list_b:
              list_tmp.append(b)
  # 转换成元组后加入到返回列表中
              resList.append(tuple(list_tmp))
  # 将刚添加的元素删除后以便进行下一轮循环
              list_tmp.remove(b)
      return resList
  
  # 获取用户输入
  list_a = input().split()
  list_b = input().split()
  
  # 调用函数
  print(unique_combinations(list_a, list_b))
  ```

### 143.编写一个程序，按照多个条件对一个元组列表进行排序。每个元组包含一个**姓名**，**年龄**和**分数**。

- 定义函数`sort_tuples()`，该函数接收一个元组列表作为参数。

- 列表中的每个元组都有三个元素：一个字符串(即姓名)和两个整数(即年龄 和 分数)。

- 如果**姓名**相同，则按照**年龄**（升序）排序；如果**姓名**和**年龄**都相同，则按照**分数**（升序）排序。

  ```python
  def sort_tuples(my_list):
      my_list.sort(key=lambda my_list: (my_list[0], my_list[1], my_list[2]))
      return my_list
  
  # 初始化列表
  my_list = []
  
  # 获取用户输入
  for _ in range(4):
      s = input()
      my_list.append(tuple(s.split(" ")))
  
  # 调用函数
  print(sort_tuples(my_list))
  ```

### 144.编写一个程序，生成斐波那契词序列的前n个元素。

- 定义函数`generate_fibonacci_word()`，接受一个参数`n`（整数）。

- 如果`n`小于**2**，函数应返回`invalid`。

- 对于`n`的其他值，生成斐波那契词序列到第n项，并逗号`, `分隔的字符串返回。

  ```python
  def generate_fibonacci_word(n):
      resList = ["a", "b"]
      if n < 2:
          return "invalid"
      elif n == 2:
          return ", ".join(resList)
      for i in range(2, n):
          tmp = resList[i - 1] + resList[i - 2]
          resList.append(tmp)
      return ", ".join(resList)
  
  # 获取用户输入
  n = int(input())
  
  # 调用函数
  print(generate_fibonacci_word(n))
  ```

### 145.编写一个程序，计算所有来自列表的质数位于质数索引位置的排列数。

- 定义函数`calculate_prime_arrangements()`，参数为一个整数`n`。

- 此函数应生成一个列表`lst = [1, 2, 3, ..., n]`。

- 它计算所有来自列表中质数位于质数索引位置的可能排列，假设列表索引从**1**开始。

- 返回这样的排列数。

  ```python
  
  ```

### 146.编写一个程序，找出给定字符串中最长有效（格式正确）括号子串的长度。

- 定义函数`length_of_longest_parentheses()`，它有一个参数`s`（字符串）。

- 在函数内部，计算并返回最长有效括号子串的长度。

  ```python
  class stack:
      def __init__(self):
          self.items = []
      def push(self,item):
          return self.items.append(item)
      def pop(self):
          if not self.isEmpty():
              return self.items.pop()
          else:
              raise LookupError('stack is empty')
      def isEmpty(self):
          return self.items == []
  if __name__ == "__main__":
      user_input = input()
      stack = stack()
      count = 0
      for i in range(0,len(user_input)):
          if user_input[i] == "(":
              stack.push(user_input[i])
          elif user_input[i] == ")" and not stack.isEmpty():
              stack.pop()
              count += 2
      print(count)
  ```

### 147.编写一个程序来确定自然数的可能分割数量。

- 定义函数`calculate_partitions()`的函数，参数为`n`。

- 在函数中，计算自然数`n`的分割数量。

  ```python
  
  ```

### 148.编写一个程序，使用正则表达式检查字符串是否与给定模式匹配。

- 定义函数`check_regex_match()`，该函数接受两个字符串参数，`input_string`和`pattern`。

- 在函数中，使用Python内置的`re`模块来实现支持`.`和`*`的正则表达式匹配。

- 如果找到匹配，则返回`True`，否则返回`False`。

  ```python
  import re
  
  def check_regex_match(input_string, pattern):
      matchtype = re.fullmatch(pattern, input_string)
      if isinstance(matchtype, re.Match):
          return True
      else:
          return False
  
  # 获取用户输入
  input_string = input()
  pattern = input()
  
  # 调用函数
  print(check_regex_match(input_string, pattern))
  ```

### 149.编写一个程序，将一个字符串(仅包含`(`或`)`)分组成括号簇，每个簇都应该是平衡的。 例如 `((()()))`是平衡的，但是`)()`是不平衡的。

- 定义函数`split_into_clusters()`，参数为`string`。

- 在函数内，将字符串拆分成平衡括号簇，并将它们作为列表返回。

  ```python
  class stack:
      def __init__(self):
          self.items = []
      def push(self, item):
          return self.items.append(item)
      def pop(self):
          if not self.isEmpty():
              return self.items.pop()
          else:
              raise LookupError('stack is empty')
      def isEmpty(self):
          return self.items == []
  if __name__ == "__main__":
      user_input = input()
      stack = stack()
      resList = []
  # 定义进栈的元素(的数目
      count1 = 0
  # 定义进栈的元素)的数目
      count2 = 0
      string = ""
      i = 0
      while i < len(user_input):
  # 当遇到(或者)时都要进行进栈的操作
          if user_input[i] == "(":
              stack.push(user_input[i])
              count1 += 1
              i += 1
          elif user_input[i] == ")":
              stack.push(user_input[i])
              count2 += 1
              i += 1
  # 当进栈的(和)的数目相等时，可以出栈。将出栈的元素存储到string中
              if count1 == count2:
                  while not stack.isEmpty():
                      string += stack.pop()
  # 注意出栈的顺序是反的，所以要进行翻转字符串的操作，然后加入到返回列表里
                  resList.append(string[::-1])
  # 出栈完成后，相关的变量值要进行初始化处理
                  count1 = 0
                  count2 = 0
                  string = ""
      print(resList)
  ```

### 150.编写一个程序，将句子中每个单词的首字母移位到下一个单词。

- 定义函数`shift_first_letter()`，参数为`sentence`（字符串）。

- 在函数内，将句子中每个单词的首字母移位到下一个单词。

- 最后一个单词的首字母移位到句子的第一个单词。

  ```python
  def shift_first_letter(sentence):
      # 将输入的字符串转换成字符串列表
      sentenceList = sentence.split(" ")
      resList = []
  # 获取首位word的第一个字符
      firstWordChar = sentenceList[0][0]
  # 获取末尾word的第一个字符
      lastWordChar = sentenceList[-1][0]
      for word in sentenceList:
  # 特殊场景：首位word的第一个字符要用末尾word的第一个字符替代
          if sentenceList.index(word) == 0:
              word = word.replace(firstWordChar, lastWordChar)
              resList.append(word)
  # 其他场景：每个单词的首位字符被前一个单词的首位字符替代
          else:
              currentChar = sentenceList[sentenceList.index(word)][0]
              previousChar = sentenceList[sentenceList.index(word) - 1][0]
              word = word.replace(currentChar, previousChar)
              resList.append(word)
  # 最终将列表转换成字符串输出
      return " ".join(resList)
  # 获取输入
  input_sentence = input()
  
  # 调用函数
  result = shift_first_letter(input_sentence)
  
  # 打印结果
  print(result)
  ```
  
  
