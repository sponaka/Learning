The Dependency Inversion Principle (DIP) states that high level modules should not depend on low level modules; both should depend on abstractions. 

Abstractions should not depend on details.  Details should depend upon abstractions. 


![image](https://user-images.githubusercontent.com/32191603/132082064-d3c33b78-838f-4987-b958-0068b4db95e2.png)


**IOC**

in traditional programming, the custom code that expresses the purpose of the program calls the reusable libraries to take care of generic tasks, but with inversion of control, it is the framework that calls the custom, or task-specific, code."


So, what the heck does that mean? Basically it means that a framework, library or any external code is not called by you, rather than it calls your code from inside itself.


https://kentcdodds.com/blog/inversion-of-control



