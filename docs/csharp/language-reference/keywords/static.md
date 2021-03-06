---
title: static 修饰符 - C# 参考
ms.date: 01/22/2020
f1_keywords:
- static
- static_CSharpKeyword
helpviewer_keywords:
- static keyword [C#]
ms.assetid: 5509e215-2183-4da3-bab4-6b7e607a4fdf
ms.openlocfilehash: e7671e9db488a7b50f4ed736864d6fa8d95eef1a
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/14/2020
ms.locfileid: "76744659"
---
# <a name="static-c-reference"></a>static（C# 参考）

使用 `static` 修饰符可声明属于类型本身而不是属于特定对象的静态成员。 `static` 修饰符可用于声明 `static` 类。 在类、接口和结构中，可以将 `static` 修饰符添加到字段、方法、属性、运算符、事件和构造函数。 `static` 修饰符不能用于索引器或终结器。 有关详细信息，请参阅[静态类和静态类成员](../../programming-guide/classes-and-structs/static-classes-and-static-class-members.md)。

## <a name="example"></a>示例

下面的类声明为 `static` 并且只含 `static` 方法：

[!code-csharp[csrefKeywordsModifiers#18](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#18)]

常数或类型声明是隐式的 `static` 成员。 不能通过实例引用 `static` 成员。 然而，可以通过类型名称引用它。 例如，请考虑以下类：

[!code-csharp[csrefKeywordsModifiers#19](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#19)]

若要引用 `static` 成员 `x`，除非可从相同范围访问该成员，否则请使用完全限定的名称 `MyBaseC.MyStruct.x`：

```csharp
Console.WriteLine(MyBaseC.MyStruct.x);
```

尽管类的实例包含该类的所有实例字段的单独副本，但每个 `static` 字段只有一个副本。

不可以使用 [`this`](this.md) 引用 `static` 方法或属性访问器。

如果 `static` 关键字应用于类，则类的所有成员都必须为 `static`。

类、接口和 `static` 类可以具有 `static` 构造函数。 在程序开始和实例化类之间的某个时刻调用 `static` 构造函数。

> [!NOTE]
> `static` 关键字比用于 C++ 中时受到的限制更多。 若要与 C++ 关键字进行比较，请参阅 [Storage classes (C++)](/cpp/cpp/storage-classes-cpp#static)（存储类 (C++)）。

若要演示 `static` 成员，请考虑表示公司员工的类。 假定此类包含计数员工的方法和存储员工人数的字段。 方法和字段均不属于任何一个员工实例。 相反，它们属于全体员工这个类。 应将其声明为该类的 `static` 成员。

## <a name="example"></a>示例

此示例读取新员工的姓名和 ID，员工计数器按 1 递增，并显示新员工信息和新员工人数。 此程序从键盘读取员工的当前人数。

[!code-csharp[csrefKeywordsModifiers#20](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#20)]  

## <a name="example"></a>示例

此示例演示了如何使用尚未声明的 `static` 字段来初始化另一个 `static` 字段。 在向 `static` 字段显式赋值之后才会定义结果。

[!code-csharp[csrefKeywordsModifiers#21](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#21)]  

## <a name="c-language-specification"></a>C# 语言规范

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>另请参阅

- [C# 参考](../index.md)
- [C# 编程指南](../../programming-guide/index.md)
- [C# 关键字](index.md)
- [修饰符](index.md)
- [静态类和静态类成员](../../programming-guide/classes-and-structs/static-classes-and-static-class-members.md)
