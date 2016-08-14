# mySpace

class Employee:
    empCount = 0
    def __init__(self, name , salary):
        self.name = name
        self.salary = salary
        Employee.empCount += 1  #class.variable

    def empName(self):
        print("Name:",self.name)
    def empIntroduce(self):
        print("Name",self.name,"Salary",self.salary)


emp = Employee('Zara',5000)
emp.empName()  #Name: Zara
emp.empIntroduce()  #Name Zara Salary 5000
print(Employee.empCount)  #1

print(hasattr(emp, 'age'))  #False
print(hasattr(emp, 'name'))  #True
print(getattr(emp, 'name'))  #Zara
setattr(emp, 'name','Lily')
print(getattr(emp, 'name'))  #Lily
delattr(emp, 'name')

print('------------')

print('类的文档字符串',Employee.__doc__)
print('类名',Employee.__name__)
print('类定义所在的模块',Employee.__module__)
print('类的所有父类构成元素',Employee.__bases__)
print('类的属性',Employee.__dict__)
