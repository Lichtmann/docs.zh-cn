---
title: -= 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.-=
helpviewer_keywords:
- -= operator [Visual Basic]
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- operator -=
- compound assignment statements [Visual Basic]
ms.assetid: 5ead0c37-ae50-48f7-8435-8e341d81cae1
ms.openlocfilehash: 44cb226d64e9f0b86c6566eb25fbafd6323a6d4c
ms.sourcegitcommit: 17ee6605e01ef32506f8fdc686954244ba6911de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2019
ms.locfileid: "74347814"
---
# <a name="--operator-visual-basic"></a>-= 运算符 (Visual Basic)
从变量或属性的值中减去表达式的值，并将结果赋给变量或属性。  
  
## <a name="syntax"></a>语法  
  
```vb  
variableorproperty -= expression  
```  
  
## <a name="parts"></a>部件  
 `variableorproperty`  
 必需。 任何数值变量或属性。  
  
 `expression`  
 必需。 任何数值表达式。  
  
## <a name="remarks"></a>备注  
 `-=` 运算符左侧的元素可以是简单的标量变量、属性或数组的元素。 变量或属性不能是[只读](../../../visual-basic/language-reference/modifiers/readonly.md)的。  
  
 `-=` 运算符首先从变量或属性（位于运算符左侧）的值中减去该表达式的值（在运算符的右侧，该表达式的值）。 然后，运算符将该操作的结果赋给变量或属性。  
  
## <a name="overloading"></a>重载  
 [-Operator （Visual Basic）](../../../visual-basic/language-reference/operators/subtraction-operator.md)可以*重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。 重载 `-` 运算符会影响 `-=` 运算符的行为。 如果你的代码在重载 `-`的类或结构上使用 `-=`，请确保了解其重新定义的行为。 有关更多信息，请参见 [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)。  
  
## <a name="example"></a>示例  
 下面的示例使用 `-=` 运算符将一个 `Integer` 变量减去另一个，并将结果赋给后一个变量。  
  
 [!code-vb[VbVbalrOperators#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#11)]  
  
## <a name="see-also"></a>另请参阅

- [-Operator （Visual Basic）](../../../visual-basic/language-reference/operators/subtraction-operator.md)
- [赋值运算符](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [算术运算符](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Visual Basic 中的运算符优先级](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [按功能列出的运算符](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [语句](../../../visual-basic/programming-guide/language-features/statements.md)
