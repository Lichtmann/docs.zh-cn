---
title: LINQ to XML 动态属性引用
ms.date: 10/22/2019
ms.topic: reference
ms.openlocfilehash: 48b51e92eb78786b2cc189e3e7daa00875b41585
ms.sourcegitcommit: 5a28f8eb071fcc09b045b0c4ae4b96898673192e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2019
ms.locfileid: "73197051"
---
# <a name="linq-to-xml-dynamic-properties"></a>LINQ to XML 动态属性

本节提供有关 LINQ to XML 中动态属性的参考信息。 具体地说，这些属性由 <xref:System.Xml.Linq.XAttribute> 命名空间中的 <xref:System.Xml.Linq.XElement> 和 <xref:System.Xml.Linq> 类公开。

如 [使用 LINQ to XML 进行 WPF 数据绑定概述](wpf-data-binding-with-linq-to-xml-overview.md) 主题中所述，每个动态属性都等效于同一类中的标准公共属性或方法。 多数情况下应使用这些标准成员；动态属性是专门为 LINQ to XML 数据绑定方案提供的。 有关这些类的标准成员的更多信息，请参见 <xref:System.Xml.Linq.XAttribute> 和 <xref:System.Xml.Linq.XElement> 参考主题。

就其解析值而论，本节中的动态属性可分为两类：

- 解析为单个值的简单动态属性，如 `Value` 和 <xref:System.Xml.Linq.XAttribute> 类中的 <xref:System.Xml.Linq.XElement> 属性。

- 解析为索引器类型的索引值，如 [Elements](elements-xelement-dynamic-property.md) 和 <xref:System.Xml.Linq.XElement> 的 [Descendants](descendants-xelement-dynamic-property.md) 属性。 对于要解析为所需值或集合的索引器类型，必须为其传递展开名称参数。

返回 <xref:System.Collections.Generic.IEnumerable%601> 类型索引值的所有动态属性都使用延迟执行。 有关延迟执行的详细信息，请参阅 [LINQ 查询简介 (C#)](../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)。

## <a name="reference"></a>参考

- <xref:System.Xml.Linq>
- <xref:System.Xml.Linq.XElement?displayProperty=fullName>
- <xref:System.Xml.Linq.XAttribute?displayProperty=fullName>

## <a name="see-also"></a>请参阅

- [使用 LINQ to XML 进行 WPF 数据绑定](wpf-data-binding-with-linq-to-xml-overview.md)
- [使用 LINQ to XML 进行 WPF 数据绑定概述](wpf-data-binding-with-linq-to-xml-overview.md)
- [LINQ 查询简介 (C#)](../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)
