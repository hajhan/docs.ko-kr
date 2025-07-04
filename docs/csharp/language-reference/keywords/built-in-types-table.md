---
title: 기본 제공 형식 표 - C# 참조
ms.custom: seodec18
description: 기본 제공 C# 형식의 키워드
ms.date: 08/17/2018
helpviewer_keywords:
- types [C#], built-in
- built-in C# types
ms.assetid: 54f901f2-bf2f-472c-ae8d-73e8ecfc57fe
ms.openlocfilehash: d93176b850d84753106accef3bcaedab38f4ddc7
ms.sourcegitcommit: a970268118ea61ce14207e0916e17243546a491f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67306793"
---
# <a name="built-in-types-table-c-reference"></a>기본 제공 형식 표(C# 참조)

다음 표에서는 <xref:System> 네임스페이스에 미리 정의된 형식의 별칭인 기본 제공 C# 형식의 키워드를 보여 줍니다.  
  
|C# 형식|.NET 형식|  
|--------------|-------------------------|  
|[bool](bool.md)|<xref:System.Boolean?displayProperty=nameWithType>|  
|[byte](byte.md)|<xref:System.Byte?displayProperty=nameWithType>|  
|[sbyte](sbyte.md)|<xref:System.SByte?displayProperty=nameWithType>|  
|[char](char.md)|<xref:System.Char?displayProperty=nameWithType>|  
|[decimal](decimal.md)|<xref:System.Decimal?displayProperty=nameWithType>|  
|[double](double.md)|<xref:System.Double?displayProperty=nameWithType>|  
|[float](float.md)|<xref:System.Single?displayProperty=nameWithType>|  
|[int](int.md)|<xref:System.Int32?displayProperty=nameWithType>|  
|[uint](uint.md)|<xref:System.UInt32?displayProperty=nameWithType>|  
|[long](long.md)|<xref:System.Int64?displayProperty=nameWithType>|  
|[ulong](ulong.md)|<xref:System.UInt64?displayProperty=nameWithType>|  
|[object](object.md)|<xref:System.Object?displayProperty=nameWithType>|  
|[short](short.md)|<xref:System.Int16?displayProperty=nameWithType>|  
|[ushort](ushort.md)|<xref:System.UInt16?displayProperty=nameWithType>|  
|[string](string.md)|<xref:System.String?displayProperty=nameWithType>|  
  
## <a name="remarks"></a>설명

`object` 및 `string`을 제외하고 표에 있는 모든 형식을 단순 형식이라고 합니다.  
  
C# 형식 키워드와 해당 별칭은 서로 바꿔서 사용할 수 있습니다. 예를 들어 다음 선언 중 하나를 사용하여 정수 변수를 선언할 수 있습니다.  

```csharp
int x = 123;
System.Int32 y = 123;
```

[typeof](../operators/type-testing-and-conversion-operators.md#typeof-operator) 연산자를 사용하여 지정된 형식을 나타내는 <xref:System.Type?displayProperty=nameWithType> 인스턴스를 가져옵니다.

```csharp
Type stringType = typeof(string);
Console.WriteLine(stringType.FullName);

Type doubleType = typeof(System.Double);
Console.WriteLine(doubleType.FullName);

// Output:
// System.String
// System.Double
```

## <a name="see-also"></a>참고 항목

- [C# 참조](../../../csharp/language-reference/index.md)
- [C# 프로그래밍 가이드](../../../csharp/programming-guide/index.md)
- [C# 키워드](index.md)
- [값 형식](value-types.md)
- [참조 형식](reference-types.md)
- [기본값 표](default-values-table.md)
- [dynamic](dynamic.md)
