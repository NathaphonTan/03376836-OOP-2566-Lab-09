# Lab 9 Exercise 4

## Override overridden Method
![alt text](./Pictures/image02.png)
1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex04
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
SecondDerivedClass sdRef  = new SecondDerivedClass();
BaseClass bcRef = (BaseClass) sdRef;

sdRef.Print();
bcRef.Print();

class BaseClass
{
    virtual public void Print()
    {
        System.Console.WriteLine("Hello from BaseClass");
    }
}
class DerivedClass : BaseClass
{
    override public void Print()
    {
       System.Console.WriteLine("Hello from DerivedClass");
    }
}
class SecondDerivedClass : DerivedClass
{
    public void Print()
    {
       System.Console.WriteLine("Hello from SecondDerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex04
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="960" alt="9 4 2" src="https://github.com/NathaphonTan/03376836-OOP-2566-Lab-09/assets/144870609/6e2dda9c-5247-4fc5-9ee4-eed19279c036">

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex04
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="960" alt="9 4 1" src="https://github.com/NathaphonTan/03376836-OOP-2566-Lab-09/assets/144870609/478e5459-7f7f-4cc6-902b-0f30ee38095b">

7.อธิบายสิ่งที่พบในการทดลอง
โปรแกรมจะแสดงผล
Hello from SecondDerivedClass
Hello from DerivedClass
