---
title: 비교 연산자 - C# 참조
description: 숫자 값 순서를 확인하는 데 사용할 수 있는 C# 비교 연산자에 대해 알아봅니다.
ms.date: 04/25/2019
author: pkulikov
f1_keywords:
- <_CSharpKeyword
- '>_CSharpKeyword'
- <=_CSharpKeyword
- '>=_CSharpKeyword'
helpviewer_keywords:
- comparison operators [C#]
- relational operators [C#]
- less than operator [C#]
- < operator [C#]
- greater than operator [C#]
- '> operator [C#]'
- less than or equal to operator [C#]
- <= operator [C#]
- greater than or equal to operator [C#]
- '>= operator [C#]'
ms.openlocfilehash: 3b123ea1ae57735cdcb763087f12c30b8008dc11
ms.sourcegitcommit: 904b98d8d706f0e2d5ceaa00ce17ffbd92adfb88
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/07/2019
ms.locfileid: "66758208"
---
# <a name="comparison-operators-c-reference"></a>비교 연산자(C# 참조)

[`<`(보다 작음)](#less-than-operator-), [`>`(보다 큼)](#greater-than-operator-), [`<=`(작거나 같음)](#less-than-or-equal-operator-) 및 [`>=`(크거나 같음)](#greater-than-or-equal-operator-) 비교는 관계형 연산자라고도 하며, 피연사자를 비교합니다. 해당 연산자는 모든 [정수](../keywords/integral-types-table.md) 및 [부동 소수점](../keywords/floating-point-types-table.md) 숫자 형식을 지원합니다.

> [!NOTE]
> `==`, `<`, `>`, `<=` 및 `>=` 연산자의 경우 피연산자 중 하나가 숫자(<xref:System.Double.NaN?displayProperty=nameWithType> 또는 <xref:System.Single.NaN?displayProperty=nameWithType>)가 아니면 연산의 결과는 `false`입니다. 즉, `NaN` 값이 `NaN`를 포함한 다른 `double`(또는 `float`) 값보다 크거나, 작거나, 같지 않습니다. 자세한 내용과 예제는 <xref:System.Double.NaN?displayProperty=nameWithType> 또는 <xref:System.Single.NaN?displayProperty=nameWithType> 참조 문서를 참조하세요.

열거형 형식은 비교 연산자도 지원합니다. 동일한 [열거형](../keywords/enum.md) 형식의 피연산자의 경우 기본 정수 형식의 해당 값이 비교됩니다.

[`==` 및 `!=` 연산자는](equality-operators.md) 피연산자가 같은지 여부를 확인합니다.

## <a name="less-than-operator-"></a>보다 작음 연산자 \<

`<` 연산자는 첫 번째 피연산자가 두 번째 피연산자보다 작으면 `true`를 반환하고, 그렇지 않으면 `false`를 반환합니다.

[!code-csharp-interactive[less than example](~/samples/csharp/language-reference/operators/ComparisonOperators.cs#Less)]

## <a name="greater-than-operator-"></a>보다 큼 연산자 >

`>` 연산자는 첫 번째 피연산자가 두 번째 피연산자보다 크면 `true`를 반환하고, 그렇지 않으면 `false`를 반환합니다.

[!code-csharp-interactive[greater than example](~/samples/csharp/language-reference/operators/ComparisonOperators.cs#Greater)]

## <a name="less-than-or-equal-operator-"></a>작거나 같음 연산자 \<=

`<=` 연산자는 첫 번째 피연산자가 두 번째 피연산자보다 작거나 같으면 `true`를 반환하고, 그렇지 않으면 `false`를 반환합니다.

[!code-csharp-interactive[less than or equal example](~/samples/csharp/language-reference/operators/ComparisonOperators.cs#LessOrEqual)]

## <a name="greater-than-or-equal-operator-"></a>크거나 같음 연산자 >=

`>=` 연산자는 첫 번째 피연산자가 두 번째 피연산자보다 크거나 같으면 `true`를 반환하고, 그렇지 않으면 `false`를 반환합니다.

[!code-csharp-interactive[greater than or equal example](~/samples/csharp/language-reference/operators/ComparisonOperators.cs#GreaterOrEqual)]

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식은 `<`, `>`, `<=` 및 `>=` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.

형식이 `<` 또는 `>` 연산자 중 하나를 오버로드하는 경우 `<` 및 `>` 모두 오버로드해야 합니다. 형식이 `<=` 또는 `>=` 연산자 중 하나를 오버로드하는 경우 `<=` 및 `>=` 모두 오버로드해야 합니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](~/_csharplang/spec/introduction.md)의 [관계형 및 형식 테스트 연산자](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- <xref:System.IComparable%601?displayProperty=nameWithType>
- [같음 연산자](equality-operators.md)
