---
title: 如何：处理查询中的复合键
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ce2f14fd-1038-458a-91e3-a078c61f0d10
ms.openlocfilehash: a6c6e7d1c1d29a049b50f4ea9d70ef5cd9e89a44
ms.sourcegitcommit: d2e1dfa7ef2d4e9ffae3d431cf6a4ffd9c8d378f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2019
ms.locfileid: "70793582"
---
# <a name="how-to-handle-composite-keys-in-queries"></a>如何：处理查询中的复合键
有些运算符只能带一个自变量。 如果您的参数必须包含数据库中的多个列，则您必须创建一个匿名类型来表示这种组合。  
  
## <a name="example"></a>示例  
 下面的示例显示了调用 `GroupBy` 运算符的查询，此运算符只能带一个 `key` 自变量。  
  
 [!code-csharp[DLinqCompositeKeys#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#1)]
 [!code-vb[DLinqCompositeKeys#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#1)]  
  
## <a name="example"></a>示例  
 联接也属于这种情况，如下例中所示：  
  
 [!code-csharp[DLinqCompositeKeys#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#2)]
 [!code-vb[DLinqCompositeKeys#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#2)]  
  
## <a name="see-also"></a>请参阅

- [查询概念](query-concepts.md)
