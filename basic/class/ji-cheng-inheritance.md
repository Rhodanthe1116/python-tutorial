# 繼承 Inheritance

{% embed url="https://learn.arcade.academy/en/latest/chapters/17_class_methods/class_methods.html#id1" %}

**在使用class時，有時候在不同的class中，需要相同功能的屬性與方法**

繼承**：**讓class保有另一個class的屬性與方法，同時又能新增或覆寫一些特有的屬性或方法



### 新增屬性或方法

###

![](<../../.gitbook/assets/image (119).png>)



由於繼承時，並不會執行父類別的建構子，因此需調用父類別的建構子，並在自己的建構子內執行





```python
class Person():
    def __init__(self):
        self.name = ""

class Employee(Person):
    def __init__(self):
        # 由於繼承時，並不會執行父類別的建構子，因此需調用父類別的建構子，並在自己的建構子內執行
        # Call the parent/super class constructor first
        super().__init__()

        # Now set up our variables
        self.job_title = ""

class Customer(Person):
    def __init__(self):
        super().__init__()
        self.email = ""

def main():
    john_smith = Person()
    john_smith.name = "John Smith"

    jane_employee = Employee()
    jane_employee.name = "Jane Employee"
    jane_employee.job_title = "Web Developer"

    bob_customer = Customer()
    bob_customer.name = "Bob Customer"
    bob_customer.email = "send_me@spam.com"

main()
```



### 覆寫屬性或方法Overriding



```python
class Person():
    def __init__(self):
        self.name = ""

    def report(self):
        # Basic report
        print("Report for", self.name)

class Employee(Person):
    def __init__(self):
        # Call the parent/super class constructor first
        super().__init__()

        # Now set up our variables
        self.job_title = ""

    def report(self):
        # Here we override report and just do this:
        print("Employee report for", self.name)

class Customer(Person):
    def __init__(self):
        super().__init__()
        self.email = ""

    def report(self):
        # Run the parent report:
        super().report()
        # Now add our own stuff to the end so we do both
        print("Customer e-mail:", self.email)

def main():
    john_smith = Person()
    john_smith.name = "John Smith"

    jane_employee = Employee()
    jane_employee.name = "Jane Employee"
    jane_employee.job_title = "Web Developer"

    bob_customer = Customer()
    bob_customer.name = "Bob Customer"
    bob_customer.email = "send_me@spam.com"

    john_smith.report()
    jane_employee.report()
    bob_customer.report()

main()
```
