# Giới thiệu một số thư viện trong Python 
## Cách tạo Module 
Module có thể được xem như là một thư viện số do chúng ta tạo, là một tệp chứa tập hợp các hàm mà mình muốn ứng dụng 
Để tạo một modulo, chúng ta đơn giản chỉ cần lưu file là đuôi mymodule.py, rồi khi muốn dùng chỉ cần khai báo "import  mymodule.py", khi sử dụng các hàm trong thư viện đó, ta thực hiện cú pháp
mymodule.(...)
Ví dụ 
 def greeting(name):
  print("Hello, " + name)
--> Lưu file thành mymodule.py

Thực hiện 
import mymodule
mymodule.greeting("Jonathan")
Thì kết quả in ra sẽ là Hello, Jonathan 

Ngoài việc chứa hàm, module còn có thể khởi tạo ra list, tuple, dictionary... Rồi khi khái báo, ta có thể sử dụng các array đã có trong module đó 
Chúng ta cũng có thể thay đổi tên của module trong lúc khai báo, ví dụ import module as np
Ta cũng có thể chọn duy nhất một hàm trong Module, bằng cách sử dụng câu lệnh from module import... 
Vd 
def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
---
from mymodule import person1

print (person1["age"])
---
Output 36


# Thư viện về thời gian của hiện tại hoặc tự thiết lập 
Ta thực hiện khai báo import datatime 
Ta có thể thực hiện một số câu lệnh như gán biến cho thời gian hiện tại 
VD
import datetime
x = datetime.datetime.now()
print(x.year)
print(x.strftime("%A"))     
(Nếu chỉ muốn in một số dữ liệu trong biến, ta có một số kí hiệu để chỉ khai báo mỗi dữ liệu đó, như trên đoạn code thì %A chính là thứ)
Hoàn toàn có thể gán biến cho một thời gian nhất định. 
vd 
import datetime
x = datetime.datetime(2020, 5, 17)
print(x)
--
output 2020,5,7

# Thư viện toán 
Đúng với cái tên, có một số kí hiệu toán học mà khi chúng ta chưa khai báo thư viện toán, chương trình sẽ báo lỗi. Ví dụ như hàm abs, tính phần nguyên, ... 

# Thư viện Json 

# Thư viện Re 
Thư viện re trong Python là công cụ chuyên dụng giúp tìm kiếm, trích xuất và xử lý chuỗi văn bản phức tạp dựa trên các quy luật mẫu.
VD
import re
txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)
if x:
  print("YES! We have a match!")
else:
  print("No match")

--
output: YES! We have a match!

