---
title: "List(1)"
published: 2025-06-09
description: "Gồm nội dung trong week 2"
image: "/images/list.png"    # Optional ảnh đại diện
tags: ["week2"]    # Tags cho bài viết
week: "week-2"
category: "Tutorial"                # Category
draft: false                        # false = publish, true = draft
---

# Nội dung bài viết

<!-- Tiêu đề căn giữa -->
<h2 style="text-align: center; margin-bottom: 5px; font-size: 40px">
  List
</h2>

<!-- Nội dung chữ và ảnh -->
<div style="display: flex; align-items: center;">
  <div style="flex: 1;">
    <p style="text-align: justify;">
      List là 1 danh sách cho phép lưu trữ nhiều giá trị cho 1 biến duy nhất. Các giá trị bao gồm (số, chuỗi, boolean, list khác,...) và các giá trị này có thể thay đổi(multable)
    </p>   
    <p style="text-align: justify;">
      list_name = [element-1,..., element-n]. Trong đó:  
    </p>
    <ul>
        <li><strong>element</strong>: các giá trị lưu trữ.</li>
        <li><strong></strong> Các giá trị được cách nhau bởi dấu phẩy.</li>
    </ul>
  </div>
  <!-- Ảnh bên phải -->
  <img 
    src="/public/images/list.png" 
    alt="Ảnh minh họa"
    style="width: 150px; height: auto; margin-left: 16px; border-radius: 8px;"
  />
</div>

### VD:
#### Danh sách kết hợp nhiều kiểu dữ liệu
```python
mixed_list = [True, 5, 'sometring', 123.45]
```
#### Danh sách số tự nhiên < 10
```python
my_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
## 🚀Indexable
Mỗi phần tử trong list đều được gắn 1 con số gọi là index
### VD:
```python
# Forward Index    0  1  2  3  4  5
data =            [4, 5, 6, 7, 8, 9]
# Backward Index  -6 -5 -4 -3 -2 -1
```
- ✅ Có thể truy cập vào phần tử trong list như sau:
```python
   data[0]  data[3]  data[-1]  data[-3]
#--> 4        7         9         7
```
```python
data = [4, 5, 6, 7, 8, 9]
print(data[-1]) # 9
print(data[-3]) # 7
```
## 🚀Slicing
Truy cập một phần các phần tử trong danh sách bằng toán tử cắt (slicing). Ta có cú pháp sau:
<div style="text-align: center; margin-bottom: 1em;">
  <p>
    <b><span style="font-size: 20px;">list[start:end:step]</span></b>
  </p>
</div>

<div>
  <p>Trong đó:</p>
  <ul>
    <li><strong>start</strong>: bắt đầu từ đâu (mặc định là 0).</li>
    <li><strong>end</strong>: dừng trước vị trí nào.</li>
    <li><strong>step</strong>: bước nhảy (mặc định là 1).</li>
  </ul>
</div>

### VD:
```python
data =            [4, 5, 6, 7, 8, 9]
# Forward Index    0  1  2  3  4  5

    data[:3]    data[2:4]    data[3:]
#--> 4 5 6         6 7        7 8 9
```
```python
data = [4, 5, 6, 7, 8, 9]
print(data[:3])  # [4 5 6]
print(data[2:4]) # [6 7]
print(data[3:])  # [7 8 9]
print(data[::2]) # [4 6 8]
print(data[:-3]) # [4 5 6]
print(data[-2:-4]) # [1: -3]
print(data[1:-3]) # [5, 6]
```
## 🚀List Method
<!-- Ảnh minh họa dưới phần List Method -->
<div style="text-align: center; margin-top: 1em;">
  <img 
    src="/public/images/list-methods.png" 
    alt="Ảnh minh họa các phương thức của list"
    style="max-width: 100%; height: auto; border-radius: 10px;"
  />
</div>

## 🚀Add elements to a Python List
- Sử dụng hàm **append()** để add **1 giá trị** vào phần cuối list.
### VD:
```python
data = [6,5,7,1,9,2]
data.append(4) #thêm 4 vào vị trí cuối list --> data = [6,5,7,1,9,2,4]
```
- Sử dụng hàm **insert()** để add **1 giá trị** vào index chỉ định trong list.
### VD:
```python
#index  0 1 2 3 4 5
data = [6,5,7,1,9,2]
data.insert(0,4) #thêm 4 vào tại vị trí index = 0 --> data = [4,6,5,7,1,9,2]
```
- Sử dụng hàm **extend** để add **các giá trị** từ các iterable khác
### VD:
```python
data = [6,5,7,1]
data.extend([9,2]) #Thêm các giá trị 9 và 2 vào vị trí cuối list --> data = [6,5,7,1,9,2]
```
- Thay đổi các phần tử của danh sách bằng cách gán giá trị mới bằng toán tử =
### VD:
```python
data = [6,5,7,1,9,2]
data[1] = 4 #Thay giá trị hiện tại của index = 1 thành 4(5 -> 4) --> data = [6,4,7,1,9,2]
```
## 🚀Delete elements to a Python List
- Sử dụng **remove()** and **pop()** để xóa 1 giá trị
### VD:
```python
data = [6,5,7,1,9,2]
data.pop(2)   #xóa giá trị tại vị trí index = 2 --> data = [6,5,1,9,2]
data.remove(5)#xóa phần tử đầu tiên có giá trị = 5 --> data = [6,7,1,9,2]
```
- Sử dụng từ khóa 'del' để xóa đối tượng hoặc hàm **clear()** để xóa hết phần tử.
### VD:
```python
data = [6,5,7,1,9,2]
del data[1:3] #xóa phần tử 1 và 2(giá trị tại index 1 và 2) --> data = [6,1,9,2]
data.clear()  #xóa hết tất cả giá trị trong list --> data = []
```
## 🚀Index() method: Returns the index of the first matched item
### VD:
```python
data = [6,5,7,1,9,2]
data.index(9) # trả về vị trí của phần tử đầu tiên có giá trị là 9 --> 4
```
## 🚀 Sử dụng hàm **Reverse()** method để đảo ngược các giá trị trong list
### VD:
```python
data = [6,5,7,1,9,2]
data.reverse() #đảo ngược các giá trị trong data --> data = [2,9,1,7,5,6]
```
## 🚀Count() method: Returns the count of the specified item in the list
### VD:
```python
data = [6,5,7,1,9,2]
data_copy = data.copy() #sao chép các giá trị có trong data --> data_copy = [6,5,7,1,9,2]
```
## 🚀Sort() method: Sorts the list in ascending/descending order
### VD:
```python
data = [6,5,7,1,9,2]
data.sort() #sắp xếp lại thứ tự các giá trị từ nhỏ đến lớn --> data = [1,2,5,6,7,9]
data.sort(reverse) #sắp xếp lại thứ tự các giá trị từ lớn đến nhỏ --> data = [9,7,6,5,2,1]
```
## 🚀Ứng dụng các toán tử + và * trong list 
### VD:
```python
data1 = [6,5,7]
data2 = [1,9,2]
data = data1 + data2 #nối 2 list lại --> data = [6,5,7,1,9,2]
```
```python
data = [6,5]
new_data = data*3 #nhân bản giá trị list theo giá trị được nhân --> new_data = [6,5,6,5,6,5]
```
## 🚀**len()**, **min()**, **max()**
### VD:
```python
data = [6,5,7,1,9,2]
len(data) #trả về độ dài của list --> 6
min(data) #trả về giá trị nhỏ nhất của list --> 1
max(data) #trả về giá trị lớn nhất của list --> 9
```
## 🚀**sum()**
### VD:
```python
data = [6,5,7,1,9,2]
sum(data) #trả về tổng tất cả giá trị trong list --> 30
```
## 🚀zip(): takes iterable containers and returns a single iterator object, having mapped values from all the containers.
### VD:
```python
data1 = [1,2,3]
data2 = [5,6,7]
for v1, v2 in zip(data1, data2): # ghép 2 list lại và so sánh từng giá trị song song nhau     1 5
    print(v1,v2)                                                                       #  --> 2 6
                                                                                       #      3 7
```
## 🚀reversed(): returns a reversed iterator object
### VD:
```python
data = [6,1,7]
reversed(data) #lật ngược vị trí các giá trị --> data = [7,1,6]
```
## 🚀Sorted(): returns a arranged list
### VD:
```python
data = [6,5,7,1,9,2]
sorted(data) #sắp xếp lại thứ tự từ nhỏ đến lớn --> data = [1,2,5,6,7,9]
sorted(data, reverse=True) #sắp xếp lại thứ tự từ lớn đến nhỏ --> data = [9,7,6,5,2,1]
```
## 🚀enumerate():  adds a counter to an iterable and returns it as an enumerate object (iterator with index and the value)
<div style="text-align: center; margin-bottom: 1em;">
  <p>
    <b><span style="font-size: 20px;">enumerate(iterable, start)</span></b>
  </p>
</div>

### VD:
```python
data = [6,1,7]                       #     0 6
for index, value in enumerate(data): #-->  1 1
    print(index, value)              #     2 7
```
```python
data = [6,1,7]                         #     7 6
for index, value in enumerate(data,7): #-->  8 1
    print(index, value)                #     9 7
```
## 🚀Practice
### ✅Sum of even number: tính tổng 2 số chẵn
<!-- Ảnh minh họa dưới phần List Method -->
<div style="text-align: center; margin-top: 1em;">
  <img 
    src="/public/images/sum1.png" 
    alt="sum of even number"
    style="max-width: 100%; height: auto; border-radius: 10px; display: block; margin: 0 auto;"
  />
</div>

### VD:
- Dùng vòng lặp for
<!-- Ảnh minh họa dưới phần List Method -->
<div style="text-align: center; margin-top: 1em;">
  <img 
    src="/public/images/sum2.png" 
    alt="Dùng vòng lặp for"
    style="max-width: 100%; height: auto; border-radius: 10px; display: block; margin: 0 auto;"
  />
</div>

```python
#Dùng vòng lặp for
def even_sum_1(data):
    result = 0

    for value in data:
        if value%2 = 0:
            result = result + value
    return result

data = [6, 5, 7, 1, 9, 2]
sum_data = even_sum_1(data)
print(sum_data) #--> 6 + 2 = 8
```
- Dùng vòng lặp while
<!-- Ảnh minh họa dưới phần List Method -->
<div style="text-align: center; margin-top: 1em;">
  <img 
    src="/public/images/sum3.png" 
    alt="Dùng vòng lặp for"
    style="max-width: 100%; height: auto; border-radius: 10px; display: block; margin: 0 auto;"
  />
</div>

```python
#Dùng vòng lặp while
def even_sum_2(data):
    result = 0
    index = 0

    while index < len(data):
        if data[index] % 2 = 0:
            result = result + data[index]
        index = index + 1
        
    return result

data = [6, 5, 7, 1, 9, 2]
sum_data = even_sum_2(data)
print(sum_data) #--> 6 + 2 = 8
```
### ✅Two sum
Tìm vị trí index của 2 giá trị mà tổng của nó bằng với giá trị được đưa ra
```markdown
data = [6,5,7,9,1,2]
target = 8
--> KQ: [2,3] # [0,5]
```
 ### VD:
```markdown
Ý tưởng giải quyết như sau:

B1: Cho 2 biến, 1 biến **num_indices** chứa các giá trị dictionary với key là giá trị của số còn value là vị trí index của số đó, 1 biến khác **ans** là list lưu các giá trị index của 2 số tổng bằng target.

B2: Dùng vòng lặp for lần lượt lướt qua các giá trị(num) và vị trí index(i) tương ứng trong list đã cho (dùng enumerate), tạo 1 biến để tính hiệu số giữa target và từng giá trị(num) trong list đã cho. Nếu kết quả của hiệu có trong biến **num_indices** thì lấy vị trí index(i) của giá trị đó với vị trí index của số đang xét trong vòng lặp for thêm vào biến **ans**.

B3: thêm giá trị num và vị trí index i vào biến **num_indices**
```
```python
def two_sum(data, target):
    num_indices = {}
    ans = []

    for i, num in enumerate(data):
        complement = target - num
        if complement in num_indices:

            ans.append([num_indices[complement], i])

        num_indices[num] = i 
        
    return ans

data = [6,5,7,1,9,2]
target = 8
result = two_sum(data, target)
print(result)
```