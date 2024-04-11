# Lab 9 Exercise 1

## Polymorphism (virtual-override methods)

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex01
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass dcRef = new DerivedClass();
BaseClass bcRef = new BaseClass();

dcRef.Info();
bcRef.Info();

class BaseClass
{
    virtual public void Info()
    {
        System.Console.WriteLine("This is BaseClass");
    }
}

class DerivedClass : BaseClass
{
    override public void Info()
    {
        System.Console.WriteLine("This is DerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex01
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="960" alt="9 1 2" src="https://github.com/NathaphonTan/03376836-OOP-2566-Lab-09/assets/144870609/5b48ba8e-0f4a-41f0-9715-b4eac4c31885">

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

<img width="960" alt="9 1 1" src="https://github.com/NathaphonTan/03376836-OOP-2566-Lab-09/assets/144870609/c11112b8-5d23-4bd5-ba19-018b11467091">

7.อธิบายสิ่งที่พบในการทดลอง
โปรแกรมจะแสดงผล
This is DerivedClass
This is BaseClass
