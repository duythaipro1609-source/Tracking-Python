# Python hướng đối tượng 
## Khai báo đối tượng trong Class 
Để khai báo một đối tượng trong Class, ta sử dụng câu lệnh __init__(self,...,...)
Trong đó, self là tên của một đối tượng, ... và ... chính là các dữ liệu liên quan đến đối tượng đó
Trong class, ta hoàn toàn có những câu lệnh dùng để xóa dữ liệu đối tượng hoặc thêm vào một dữ liệu đối tượng, đó chính là del và khai báo trực tiếp khi mà đã khởi tạo xong 
VD
class Car
     def __init__(self,brand,colour)
     self.brand=brand #.brand tức là tên của dữ liệu brand, ta hoàn toàn có thể đổi được
     self.coulour=colour
#Khai báo đối tượng
car1= Car("Car", "Ford" )  #Đối tượng car, có hiệu là Ford 
car1.price = (2500) #Thêm dữ liệu giá 
del car1.brand #Xóa dữ liệu giá

Trong class, ta hoàn toàn có thể nhiều hàm rồi ứng dụng nó vào đối tượng 
VD
class Calculator:
  def add(self, a, b):
    return a + b
  def multiply(self, a, b):
    return a * b
calc = Calculator()
print(calc.add(5, 3))
print(calc.multiply(4, 7))
## Class parent
Trong Python hướng đối tượng, ta hoàn toàn có thể xây dựng các lớp là con của lớp khác, từ đó sử dụng các thuộc tính của lớp Parent để sử dụng và xây dựng 
