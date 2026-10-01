# Tổng hợp các kiến thức
Trong xuyên suốt báo cáo, nếu một đoạn văn bản được bắt đầu bởi dấu ~~ và kết thúc bởi dấu ~~ thì ta sẽ hiểu đoạn văn bản đó là 1 mã code Python
Còn với màn hình in ra, ở đầu văn bản sẽ có kí hiệu -- và cuối văn bản sẽ là --
Để trình bày một cách dễ hiểu, thì chủ yếu sẽ lấy ví dụ của từng kiểu kiến thức trong Python, các phép toán, hàm, lệnh sử dụng trong kiến thức đó sẽ được ví dụ trực tiếp
## 1: Danh sách (List) trong Python
Cách khai báo, triển khai:
~~
ten_bien = ["ManCity", "Real Madrid", "Manchester United"]
math_scores= [1,2,3,4]
~~
Danh sách là một kiểu liệt kê các phần tử có kể cả thứ tự, có thể chỉnh sửa được
Các phần tử được đếm với phần tử đầu tiên có STT là 0. Có thể quy ước phần tử cuối là -1, các phần tử sau mang STT giảm dần.
Cách in ra phần từ i mà mình muốn, thực hiện câu lệnh 
~~
print(ten_bien[1])
print(ten_bien[-1])
~~
Khi đó
--
Real Madrid
"Manchester United
--
Danh sách còn có thể lấy 1 phần tử
VD
~~
print(ten_bien[1:2])
~~
--
Real Madrid
--
Ngoài ra, còn có một số câu lệnh phổ biến như sau:
Sửa giá trị phần tử trong List:
~~
ten_bien[1] = "Arsenal"  # Thay đổi phần tử ở vị trí số 1 thành "Arsenal"
~~
Nối danh sách (extend): Thêm một danh sách vào cuối danh sách hiện tại.
~~
ten_bien.extend(math_scores) # Nối tiếp danh sách math_scores vào cuối danh sách ten_bien
~~
Thêm phần tử vào cuối (append):
~~
ten_bien.append("AC MILAN")  #Nối tiếp danh sách bằng cách thêm phần tử vào cuối 
~~
Chèn phần tử vào vị trí bất kỳ (insert): Nhận 2 tham số:
~~
ten_bien.insert(1, "Chelsea") # Chèn "Dũng" vào vị trí số 1 #Thêm phần tử Chelsea vào thứ tự 1
~~
Xóa phần tử theo giá trị (remove):
~~
ten_bien.remove("Real Madrid)
~~
Xóa toàn bộ phần tử (clear)
... 
Tìm vị trí phần tử (index):
~~
student_names = ["An", "Hưng", "Tuyên"]
print(student_names.index("Tuyên")) # Trả về chỉ số vị trí của phần tử
~~
Đếm số lần xuất hiện (count):
~~
student_names = ["Nguyên", "Hưng", "Nguyên", "Sáng"]
print(student_names.count("Nguyên")) # Đếm số lần xuất hiện
~~
## Tuple
Tuple tương tự như List nhưng sử dụng dấu ngoặc tròn (), nhưng không thể thay đổi, thêm, sửa, xóa các phần tử sau khi đã khởi tạo . 
Cách khai báo và truy cập phần tử:
~~
coordinate = (123, 456)
print(coordinate[0]) # In phần tử đầu tiên
print(coordinate[1]) # In phần tử thứ hai
~~
(Lưu ý: Nếu cố gắng gán lại giá trị như coordinate[1] = 789, Python sẽ báo lỗi TypeError vì Tuple không hỗ trợ thay đổi).

## Hàm trong Python
Hàm là một tập hợp các câu lệnh được gom lại để thực thi một nhiệm vụ, bài toán.
Cách định nghĩa và gọi hàm không có tham số:
~~
def say_hello():    # Gọi hàm để thực thi
print("Chào mừng bạn đến với Python") 
~~
Câu lệnh return trong hàm
Lệnh return dùng để trả về một giá trị từ hàm sau khi tính toán xong.
~~
def add(a, b):
return a + b # Trả về tổng của a và b

result = add(4, 6)
print(result)
~~
## Câu lệnh điều kiện if, elif, else
Cho phép chương trình rẽ nhánh và ra quyết định dựa trên các điều kiện so sánh.

~~
a = 200
b = 100

if a < b:
print("A nhỏ hơn B")
elif a > b:
print("A lớn hơn B")
else:
print("A bằng B")
~~
A lớn hơn B
7: Toán tử logic (and, or, not)
Dùng để kết hợp nhiều điều kiện trong câu lệnh điều kiện.

Toán tử and (Đúng khi tất cả các vế đều đúng):
~~
a = 200
b = 50
c = 100
if a > b and a > c:
print("A là số lớn nhất")
~~
--
A là số lớn nhất
--

Toán tử or (Đúng khi có ít nhất một vế đúng):
~~
a = 100
b = 50
c = 100
if a == b or a == c:
print("Có ít nhất một số bằng với giá trị của A")
~~
--
Có ít nhất một số bằng với giá trị của A
--

Toán tử not (Đảo ngược giá trị True/False):
~~
a = 100
b = 200
if not a > b:
print("A không lớn hơn B")
~~
--
A không lớn hơn B
--

## Cấu trúc dữ liệu Dictionary
Dictionary lưu trữ dữ liệu dưới dạng các cặp Key - Value, sử dụng dấu ngoặc nhọn {}. Các Key trong từ điển phải là duy nhất.

Cách khai báo và truy cập dữ liệu:
~~
english_vietnamese_dictionary = {
"Hello": "Xin chào",
"Goodbye": "Tạm biệt"
}

Truy cập bằng Key hoặc hàm get()
print(english_vietnamese_dictionary["Hello"])
print(english_vietnamese_dictionary.get("Goodbye"))
print(english_vietnamese_dictionary.get("cat", "Từ khóa này không tồn tại"))
~~
Xin chào
Tạm biệt
Từ khóa này không tồn tại
## Vòng lặp while
Thực thi khối lệnh lặp đi lặp lại miễn là điều kiện kiểm tra còn đúng (True).

~~
i = 1
while i < 4:
print("Meo meo")
i += 1
print("Được rồi tôi cho bạn ăn đây")
~~
Meo meo
Meo meo
Meo meo
Được rồi tôi cho bạn ăn đây
## Vòng lặp for
Dùng để duyệt qua từng phần tử của chuỗi, danh sách hoặc một dãy số (range).

~~

Duyệt qua chuỗi ký tự
for character in "Sáng":
print(character)

Sử dụng hàm range để lặp từ 1 đến 3
~~
for index in range(1, 4):
print(index)
~~
--
1
2
3
--












