---
Course: C212 Java
Date: 2025-04-02
---
```Java
class SalaryEmployee
		private int salary;
		private String name;
		private int age;
SalaryEmployee(String name, int age, int salary) {
		super(name, age);
		this.salary =  salary;
}
		
```

- B is a subclass of A if B extends A
- How do we call a subclass
    - super( a, b)
- how do we create a new Employee instance
    
    - Emp e = new Emp(”A”, 100)
    - SalaryEmployee se = new SalaryEmployee(”B”, 25, 50000)
    - What happens with this? Emp e2 = new SalaryEmployee(”C, 30, 40000);
        - gives you C, 30, 40000
    
      
    
    ```Java
    Emp e2 = newS SalaryEmployee("C", 30, 40000);
    		((SalaryEmployee)e^2).getSalary()
    ```
    

### Object

- toString()
- hashCode()
- equals(Object o)

```Java
@Override
public boolean equals(Object o) {
			if(!(o instanceof Employee))return false
			} else {
					Emplyee othEmp = (Employee) o;
					return this.name .equals
```