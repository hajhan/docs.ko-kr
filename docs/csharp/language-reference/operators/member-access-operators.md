---
title: 멤버 액세스 연산자 - C# 참조
description: 형식 멤버에 액세스하는 데 사용하는 C# 연산자에 대해 알아봅니다.
ms.date: 05/09/2019
author: pkulikov
f1_keywords:
- ._CSharpKeyword
- '[]_CSharpKeyword'
- ()_CSharpKeyword
helpviewer_keywords:
- member access operators [C#]
- member access operator [C#]
- dot operator [C#]
- . operator [C#]
- subscript operator [C#]
- square brackets [] operator [C#]
- indexer operator [C#]
- '[] operator [C#]'
- null-conditional operators [C#]
- Elvis operator [C#]
- ?. operator [C#]
- ?[] operator [C#]
- invocation operator [C#]
- method call [C#]
- method invocation [C#]
- delegate invocation [C#]
- () operator [C#]
ms.openlocfilehash: de0715a2ac946fa47f0d83ac8569595e622f0b97
ms.sourcegitcommit: 904b98d8d706f0e2d5ceaa00ce17ffbd92adfb88
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/07/2019
ms.locfileid: "66758089"
---
# <a name="member-access-operators-c-reference"></a>멤버 액세스 연산자(C# 참조)

형식 멤버에 액세스할 때 다음과 같은 연산자를 사용할 수 있습니다.

- [`.` (멤버 액세스)](#member-access-operator-): 네임스페이스 또는 형식의 멤버 액세스
- [`[]` (배열 요소 또는 인덱서 액세스)](#indexer-operator-): 배열 요소 또는 형식 인덱서 액세스
- [`?.` 및 `?[]`(null 조건부 연산자)](#null-conditional-operators--and-): 피연산자가 null이 아닌 경우에만 멤버 또는 요소 액세스 작업 수행
- [`()` (호출)](#invocation-operator-): 액세스된 메서드나 대리자 호출

## <a name="member-access-operator-"></a>멤버 액세스 연산자

다음 예제와 같이 `.` 토큰을 사용하여 네임스페이스 또는 형식의 멤버에 액세스합니다.

- [ `using` 지시문](../keywords/using-directive.md)의 다음 예제와 같이 `.`을 사용하여 네임스페이스 내에 중첩된 네임스페이스에 액세스합니다.

  [!code-csharp[nested namespaces](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#NestedNamespace)]

- 다음 코드와 같이 `.`을 사용하여 ‘정규화된 이름’을 만들고 네임스페이스 내의 형식에 액세스합니다. 

  [!code-csharp[qualified name](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#QualifiedName)]

  [`using` 지시문](../keywords/using-directive.md)을 사용하여 정규화된 이름 사용을 선택 사항으로 설정합니다.

- 다음 코드와 같이 `.`을 사용하여 정적 및 비정적 [형식 멤버](../../programming-guide/classes-and-structs/index.md#members)에 액세스합니다.

  [!code-csharp-interactive[type members](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#TypeMemberAccess)]

`.`을 사용하여 [확장 메서드](../../programming-guide/classes-and-structs/extension-methods.md)에 액세스할 수도 있습니다.

## <a name="indexer-operator-"></a>인덱서 연산자 []

대괄호 `[]`는 일반적으로 배열, 인덱서 또는 포인터 요소 액세스에 사용됩니다.

### <a name="array-access"></a>배열 액세스

다음 예제는 배열 요소에 액세스하는 방법을 보여 줍니다.

[!code-csharp-interactive[array access](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#Arrays)]

배열 인덱스가 배열의 해당 차원 범위를 벗어난 경우 <xref:System.IndexOutOfRangeException>이 throw됩니다.

앞의 예제와 같이, 배열 형식을 선언하거나 배열 인스턴스를 인스턴스화할 때도 대괄호를 사용합니다.

배열에 대한 자세한 내용은 [배열](../../programming-guide/arrays/index.md)을 참조하세요.

### <a name="indexer-access"></a>인덱서 액세스

다음 예제는 .NET <xref:System.Collections.Generic.Dictionary%602> 형식을 사용하여 인덱서 액세스를 보여 줍니다.

[!code-csharp-interactive[indexer access](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#Indexers)]

인덱서를 사용하면 배열 인덱싱과 비슷한 방법으로 사용자 정의 형식의 인스턴스를 인덱싱할 수 있습니다. 정수여야 하는 배열 인덱스와 달리, 인덱서 인수는 임의 형식으로 선언할 수 있습니다.

인덱서에 대한 자세한 내용은 [인덱서](../../programming-guide/indexers/index.md)를 참조하세요.

### <a name="other-usages-of-"></a>다른 [] 용도

포인터 요소 액세스에 대한 자세한 내용은 [포인터 관련 연산자](pointer-related-operators.md) 문서의 [포인터 요소 액세스 연산자](pointer-related-operators.md#pointer-element-access-operator-) 섹션을 참조하세요.

또한 대괄호를 사용하여 [특성](../../programming-guide/concepts/attributes/index.md)을 지정합니다.

```csharp
[System.Diagnostics.Conditional("DEBUG")]
void TraceMethod() {}
```

## <a name="null-conditional-operators--and-"></a>Null 조건부 연산자 ?. 및 ?[]

C# 6 이상에서 사용할 수 있는 null 조건부 연산자는 피연산자가 null이 아닌 것으로 평가되었을 때만 멤버 액세스 `?.`, 또는 요소 액세스 `?[]` 연산을 피연산자에게 적용합니다. 피연산자가 `null`로 평가되면 연산자 적용 결과가 `null`입니다. Null 조건부 멤버 액세스 연산자 `?.`를 Elvis 연산자라고도 합니다.

Null 조건부 연산자는 단락 연산자입니다. 즉 조건부 멤버나 요소 액세스 작업의 한 체인의 작업에서 `null`을 반환하면 나머지 체인은 실행되지 않습니다. 다음 예제에서 `A`가 `null`로 평가되면 `B`가 평가되지 않고, `A` 또는 `B`가 `null`로 평가되면 `C`가 평가되지 않습니다.

```csharp
A?.B?.Do(C);
A?.B?[C];
```

다음 예제에서는 `?.` 및 `?[]` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[null-conditional operators](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#NullConditional)]

위의 예제에서는 [null 병합 연산자](null-coalescing-operator.md)의 사용법도 보여 줍니다. null 병합 연산자를 사용하여 null 조건부 연산 결과가 `null`인 경우 평가하는 대체 식을 제공할 수 있습니다.

### <a name="thread-safe-delegate-invocation"></a>스레드로부터 안전한 대리자 호출

다음 코드에서처럼 `?.` 연산자를 사용하여 대리자가 null이 아닌지 확인하고 스레드로부터 안전한 방식으로 호출합니다(예: [이벤트 발생 시](../../../standard/events/how-to-raise-and-consume-events.md)).

```csharp
PropertyChanged?.Invoke(…)
```

이 코드는 C# 5 및 그 이전에서 사용하는 다음 코드에 해당합니다.

```csharp
var handler = this.PropertyChanged;
if (handler != null)
{
    handler(…);
}
```

## <a name="invocation-operator-"></a>호출 연산자()

괄호(`()`)를 사용하여 [메서드](../../programming-guide/classes-and-structs/methods.md) 또는 [대리자](../../programming-guide/delegates/index.md)를 호출합니다.

다음 예제는 인수를 사용하거나 사용하지 않고 메서드를 호출하는 방법과 대리자를 호출하는 방법을 보여 줍니다.

[!code-csharp-interactive[invocation with ()](~/samples/csharp/language-reference/operators/MemberAccessOperators.cs#Invocation)]

[`new`](../keywords/new-operator.md) 연산자를 사용하여 [생성자](../../programming-guide/classes-and-structs/constructors.md)를 호출하는 경우에도 괄호를 사용합니다.

### <a name="other-usages-of-"></a>다른 () 용도

또한 괄호를 사용하여 식에서 연산을 계산하는 순서를 지정합니다. 자세한 내용은 [연산자](../../programming-guide/statements-expressions-operators/operators.md) 문서의 [괄호 추가](../../programming-guide/statements-expressions-operators/operators.md#adding-parentheses) 섹션을 참조하세요. 우선 순위 수준에 따라 정렬된 연산자 목록은 [C# 연산자](index.md)를 참조하세요.

전환 연산자를 호출하는 [캐스트 식](invocation-operator.md#cast-expression)도 괄호를 사용합니다.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

`.` 및 `()` 연산자는 오버로드할 수 없습니다. `[]` 연산자도 오버로드할 수 없는 연산자로 간주됩니다. [인덱서](../../programming-guide/indexers/index.md)를 사용하여 사용자 정의 형식의 인덱싱을 지원합니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](~/_csharplang/spec/introduction.md)의 다음 섹션을 참조하세요.

- [멤버 액세스](~/_csharplang/spec/expressions.md#member-access)
- [요소 액세스](~/_csharplang/spec/expressions.md#element-access)
- [Null 조건부 연산자](~/_csharplang/spec/expressions.md#null-conditional-operator)
- [호출 식](~/_csharplang/spec/expressions.md#invocation-expressions)

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [??(Null 병합 연산자)](null-coalescing-operator.md)
