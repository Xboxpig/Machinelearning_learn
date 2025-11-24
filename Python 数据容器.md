
| 名称  | 英文    | 符号  | 可变？  | 访问数据            |
| --- | ----- | --- | ---- | --------------- |
| 元组  | Tuple | ( ) | 不可变的 | 索引位置 tuple[0]   |
| 列表  | list  | [ ] | 可变的  | 索引位置 list[0]    |
| 字典  | dict  | { } | 可变的  | 标签 dict['name'] |

## Tuple用法
```
my_tuple = (10, 20, 30)
# my_tuple[0] = 99  <-- 试图执行会报错 (TypeError)
# 访问：>>> my_tuple[0]
			10
```

## List用法

```
my_list = ['apple', 'banana', 'cherry']
my_list[0] = 'orange'  # 可以修改
my_list.append('grape')  # 可以添加
# 访问：my_list[0] 是 'orange'
```

## Dict用法

dict包括key value，键值对，key相当是一个带名称的索引，value是其值 *(可以是数值或者是字符)

```
my_dict = {'name': 'Bob', 'age': 35, 'city': 'London'}
my_dict['age'] = 36  # 可以修改
# 访问：my_dict['name'] 是 'Bob'
```
