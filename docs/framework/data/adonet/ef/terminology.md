---
title: Entity Framework 용어
ms.date: 03/30/2017
ms.assetid: fa2a1bd1-6118-487b-8673-eebc66b92945
ms.openlocfilehash: 53a6888d0b32cfeb73e7254dc0778274fe6cd0eb
ms.sourcegitcommit: a970268118ea61ce14207e0916e17243546a491f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67306346"
---
# <a name="entity-framework-terminology"></a>Entity Framework 용어
이 항목에서는 자주 참조 되는 용어를 정의 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] 설명서. 추가 정보를 볼 수 있는 관련 항목에 대한 링크가 제공됩니다.  
  
|용어|정의|  
|----------|----------------|  
|연결(association)|엔터티 형식 간의 관계 정의입니다.<br /><br /> 자세한 내용은 [Association 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#association-element-csdl) 하 고 [연결 형식](../../../../../docs/framework/data/adonet/association-type.md)합니다.|  
|연결 집합(association set)|같은 형식의 연결 인스턴스를 위한 논리 컨테이너입니다.<br /><br /> 자세한 내용은 [AssociationSet 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#associationset-element-csdl) 하 고 [연결 집합](../../../../../docs/framework/data/adonet/association-set.md)합니다.|  
|Code First|Entity Framework 4.1부터는 Code First 개발을 통해 모델을 프로그램 방식으로 만들 수 있습니다. Code First 개발에는 두 가지 다른 시나리오가 있습니다. 두 경우 모두 개발자는 .NET Framewor 클래스 정의를 코딩하여 모델을 정의한 후 데이터 주석 또는 fluent API를 사용하여 추가 매핑 또는 구성을 선택적으로 지정합니다.<br /><br /> Code First 개발에 포함 되어 있는지를 확인 합니다 [Entity Framework 5.0](https://go.microsoft.com/fwlink/?LinkId=234900)합니다. Entity Framework 5.0은 .NET Framework의 일부가 아니지만 .NET Framework 4.5에 빌드되어 있습니다. Entity Framework 5.0은로 제공 합니다 [' Entity Framework'](https://go.microsoft.com/fwlink/?LinkID=215714)[NuGet](https://go.microsoft.com/fwlink/?LinkId=232488) 패키지 있습니다. 자세한 내용은 [Entity Framework 릴리스 및 버전 관리](https://go.microsoft.com/fwlink/?LinkId=234899)합니다.|  
|명령 트리|모든 일반적인 프로그래밍 방식 표현 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] 하나 이상의 식으로 구성 되는 쿼리.<br /><br /> 자세한 내용은 [Entity Framework 개요](../../../../../docs/framework/data/adonet/ef/overview.md)합니다.|  
|복합 형식|개념적 모델에서 정의된 복합 속성을 나타내는 .NET Framework 클래스입니다. 복합 형식을 사용하면 엔터티 내에 스칼라 속성을 구성할 수 있습니다. 복합 개체는 복합 형식의 인스턴스입니다. 자세한 내용은 [ComplexType 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#complextype-element-csdl) 하 고 [복합 형식](../../../../../docs/framework/data/adonet/complex-type.md)합니다.|  
|ComplexType|키 속성이 없는, 엔터티 형식의 스칼라가 아닌 속성을 나타내는 데이터 형식의 지정입니다.<br /><br /> 자세한 내용은 [ComplexType 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#complextype-element-csdl) 하 고 [복합 형식](../../../../../docs/framework/data/adonet/complex-type.md)합니다.|  
|개념 모델(conceptual model)|[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]의 응용 프로그램 도메인에 있는 엔터티 형식, 복합 형식, 연결, 엔터티 컨테이너, 엔터티 집합 및 연결 집합의 추상 지정입니다. 개념적 모델은 .csdl 파일에 CSDL로 정의됩니다.<br /><br /> 자세한 내용은 [모델링 및 매핑](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)합니다.|  
|.csdl 파일|CSDL로 표현된 개념적 모델이 포함된 XML 파일입니다.|  
|CSDL(개념 스키마 정의 언어)|개념 모델의 엔터티 형식, 연결, 엔터티 컨테이너, 엔터티 집합 및 연결 집합을 정의하는 데 사용되는 XML 기반 언어입니다.<br /><br /> 자세한 내용은 [CSDL Specification](../../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)을 참조하십시오.|  
|컨테이너|엔터티 및 연결 집합의 논리적 그룹입니다.<br /><br /> 자세한 내용은 [EntityContainer 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#entitycontainer-element-csdl) 하 고 [엔터티 컨테이너](../../../../../docs/framework/data/adonet/entity-container.md)합니다.|  
|동시성|여러 사용자가 동시에 공유 데이터에 액세스하여 변경할 수 있도록 하는 프로세스입니다. 기본적으로 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]에서는 낙관적 동시성 모델을 구현합니다.|  
|방향|일부 연결의 비대칭 특성을 나타냅니다. 방향은 스키마에 있는 `FromRole` 또는 `ToRole` 요소의 `NavigationProperty` 및 `ReferentialConstraint` 특성으로 지정됩니다.<br /><br /> 자세한 내용은 [NavigationProperty 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#navigationproperty-element-csdl) 하 고 [탐색 속성](../../../../../docs/framework/data/adonet/navigation-property.md)합니다.|  
|즉시 로드(eager loading)|쿼리에서 명시적으로 요청된 개체와 함께 특정한 관련 개체 집합을 로드하는 프로세스입니다.|  
|.edmx 파일|CSDL로 표현된 개념적 모델, SSDL로 표현된 저장소 모델, MSL로 표현된 두 모델 간의 매핑이 포함된 XML 파일입니다. .Edmx 파일은 엔터티 데이터 모델 도구에서 생성 됩니다. 자세한 내용은 [.edmx 파일 개요](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))합니다.|  
|end|연결에 참여하는 엔터티입니다.<br /><br /> 자세한 내용은 [끝 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#end-element-csdl) 하 고 [연결 end](../../../../../docs/framework/data/adonet/association-end.md)합니다.|  
|entity|데이터 형식을 정의하는 데 사용되는 응용 프로그램 도메인의 개념입니다.<br /><br /> 자세한 내용은 [EntityType 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#entitytype-element-csdl) 하 고 [엔터티 형식](../../../../../docs/framework/data/adonet/entity-type.md)합니다.|  
|EntityClient|와 같은 클래스를 포함 하는 저장소에 독립적인 ADO.NET 데이터 공급자 `EntityConnection`, `EntityCommand`, 및 `EntityDataReader`합니다. 협력 [!INCLUDE[esql](../../../../../includes/esql-md.md)] 와 같은 저장소 특정 ADO.NET 데이터 공급자에 연결 하 고 `SqlClient`입니다.<br /><br /> 자세한 내용은 [Entity Framework 용 EntityClient 공급자](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)합니다.|  
|엔터티 컨테이너(entity container)|지정한 네임스페이스에서 구현될 엔터티 집합과 연결 집합을 지정합니다.<br /><br /> 자세한 내용은 [EntityContainer 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#entitycontainer-element-csdl) 하 고 [엔터티 컨테이너](../../../../../docs/framework/data/adonet/entity-container.md)합니다.|  
|EDM(엔터티 데이터 모델)|저장된 폼에 관계없이 데이터 구조를 엔터티와 관계로 설명하는 개념 집합입니다.<br /><br /> 자세한 내용은 [엔터티 데이터 모델](../../../../../docs/framework/data/adonet/entity-data-model.md)합니다.|  
|Entity Framework|개발자가 데이터 소스의 논리 스키마에 매핑된 개념적 모델을 사용할 수 있도록 하여 데이터 지향 소프트웨어 응용 프로그램의 개발을 지원하는 기술 집합입니다.<br /><br /> 자세한 내용은 [Entity Framework 개요](../../../../../docs/framework/data/adonet/ef/overview.md)합니다.|  
|엔터티 집합|지정된 형식 및 해당 하위 형식의 엔터티를 위한 논리적 컨테이너입니다. 엔터티 집합은 데이터베이스 테이블에 매핑됩니다.<br /><br /> 자세한 내용은 [EntitySet 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#entityset-element-csdl) 하 고 [엔터티 집합](../../../../../docs/framework/data/adonet/entity-set.md)합니다.|  
|Entity SQL|개념적 엔터티 스키마를 직접 사용하며 상속 및 관계와 같은 개념적 모델 개념을 지원하는, 저장소에 독립적인 SQL 언어입니다.<br /><br /> 자세한 내용은 [Entity SQL 언어](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)합니다.|  
|엔터티 형식(entity type)|개념적 모델에 정의 된 대로 엔터티를 나타내는.NET Framework 클래스입니다. 엔터티 형식은 스칼라, 복합 및 탐색 속성을 가질 수 있습니다. 개체는 엔터티 형식의 인스턴스입니다. 자세한 내용은 [개체를 사용 하 여 작업](../../../../../docs/framework/data/adonet/ef/working-with-objects.md)합니다.|  
|EntityType|키와 명명된 속성 집합을 포함하고 개념적 모델 또는 저장소 모델의 최상위 항목을 나타내는 데이터 형식의 지정입니다.<br /><br /> 자세한 내용은 [EntityType 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#entitytype-element-csdl) 하 고 [엔터티 형식](../../../../../docs/framework/data/adonet/entity-type.md)합니다.|  
|명시적 로드(explicit loading)|개체가 쿼리에서 반환될 때 관련 개체가 동시에 로드되지 않습니다. 기본적으로 탐색 속성의 `Load` 메서드를 사용하여 명시적으로 요청할 때까지 관련 개체는 로드되지 않습니다.|  
|외래 키 연결|외래 키 속성을 통해 관리되는 엔터티 간의 연결입니다.|  
|식별 관계|주 엔터티의 기본 키가 종속 엔터티의 기본 키에 속하는 관계입니다. 이러한 종류의 관계에서 종속 엔터티는 주 엔터티 없이 존재할 수 없습니다.|  
|독립 연결|독립 개체에 의해 표현되고 추적되는 엔터티 간의 연결입니다.|  
|key|엔터티 형식의 고유한 인스턴스를 식별하는 데 사용되는 속성 또는 속성 집합을 지정하는 엔터티 형식의 특성입니다. <xref:System.Data.EntityKey> 클래스에 의해 개체 계층에서 표현됩니다.<br /><br /> 자세한 내용은 [Key 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#key-element-csdl) 하 고 [엔터티 키](../../../../../docs/framework/data/adonet/entity-key.md)합니다.|  
|지연 로드|개체가 쿼리에서 반환될 때 관련 개체가 동시에 로드되지 않습니다. 대신 탐색 속성에 액세스하면 관련 개체가 자동으로 로드됩니다.|  
|[!INCLUDE[linq_entities](../../../../../includes/linq-entities-md.md)]|통과, 필터 및 프로젝션 작업 Visual C# 및 Visual Basic에서 직접적이 고 선언적인 방식으로 표현할 수 있도록 하는 쿼리 연산자 집합을 정의 하는 쿼리 구문입니다.<br /><br /> 자세한 내용은 [LINQ to Entities](../../../../../docs/framework/data/adonet/ef/language-reference/linq-to-entities.md)합니다.|  
|매핑|개념적 모델에 있는 항목과 저장소 모델에 있는 항목 간의 대응 지정입니다.<br /><br /> 자세한 내용은 [MSL 사양](../../../../../docs/framework/data/adonet/ef/language-reference/msl-specification.md)합니다.|  
|.msl 파일|MSL로 표현된, 개념적 모델과 저장소 모델 간의 매핑이 포함된 XML 파일입니다.|  
|MSL(매핑 사양 언어)|개념 모델에서 정의한 항목을 저장소 모델의 항목에 매핑하는 데 사용되는 XML 기반 언어입니다.<br /><br /> 자세한 내용은 [MSL 사양](../../../../../docs/framework/data/adonet/ef/language-reference/msl-specification.md)합니다.|  
|수정 함수|데이터 소스에 있는 데이터를 삽입, 업데이트 및 삭제하는 데 사용되는 저장 프로시저입니다. 이러한 함수는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]에서 생성된 명령 대신 사용됩니다. 수정 함수는 저장소 모델의 `Function` 요소에 의해 정의됩니다. 합니다 [ModificationFunctionMapping](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716778(v=vs.100)) 요소는 이러한 수정 함수를 삽입, 업데이트 및 삭제 개념적 모델에 정의 된 엔터티에 대 한 작업을 매핑합니다.|  
|복합성|연결에서 정의된 대로 관계의 양쪽에 존재할 수 있는 엔터티 수입니다. 카디널리티라고도 합니다.<br /><br /> 자세한 내용은 [끝 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#end-element-csdl) 하 고 [연결 end](../../../../../docs/framework/data/adonet/association-end.md)합니다.|  
|형식별 다중 엔터티 집합|둘 이상의 엔터티 집합에서 같은 엔터티 형식을 정의할 수 있는 기능입니다.<br /><br /> 자세한 내용은 [EntitySet 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#entityset-element-csdl) 고 [방법: 형식별 다중 엔터티 집합을 사용 하 여 모델 정의](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738537(v=vs.100))합니다.|  
|탐색 속성(navigation property)|연결에서 정의된 대로 다른 엔터티 형식에 대한 관계를 나타내는 엔터티 형식의 속성입니다. 탐색 속성은 연결에서 반대쪽 End의 복합성에 따라 관련 개체를 <xref:System.Data.Objects.DataClasses.EntityCollection%601> 또는 <xref:System.Data.Objects.DataClasses.EntityReference%601>로 반환하는 데 사용됩니다.<br /><br /> 자세한 내용은 [NavigationProperty 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#navigationproperty-element-csdl) 하 고 [탐색 속성](../../../../../docs/framework/data/adonet/navigation-property.md)합니다.|  
|쿼리 경로|개체 쿼리가 실행될 때 반환할 관련 개체를 지정하는 경로의 문자열 표현입니다. 쿼리 경로는 <xref:System.Data.Objects.ObjectQuery%601.Include%2A>의 <xref:System.Data.Objects.ObjectQuery%601> 메서드를 호출하여 정의됩니다.<br /><br /> 자세한 내용은 [관련 개체 로드](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896272(v=vs.100))합니다.|  
|개체 컨텍스트|개념적 모델에서 정의된 엔터티 컨테이너를 나타냅니다. 기본 데이터 소스에 대한 연결을 포함하며, 변경 내용 추적 및 ID 확인과 같은 서비스를 제공합니다. 개체 컨텍스트는 <xref:System.Data.Objects.ObjectContext> 또는 `DbContext` 클래스 인스턴스로 표현됩니다.<br /><br /> `DbContext` 일부인 합니다 [Entity Framework 5.0](https://go.microsoft.com/fwlink/?LinkId=234900)합니다. Entity Framework 5.0은 .NET Framework의 일부가 아니지만 .NET Framework 4.5에 빌드되어 있습니다. Entity Framework 5.0은로 제공 합니다 [' Entity Framework'](https://go.microsoft.com/fwlink/?LinkID=215714)[NuGet](https://go.microsoft.com/fwlink/?LinkId=232488) 패키지 있습니다. 자세한 내용은 [Entity Framework 릴리스 및 버전 관리](https://go.microsoft.com/fwlink/?LinkId=234899)합니다.|  
|개체 계층|Entity Framework에서 사용되는 엔터티 형식 및 개체 컨텍스트 정의입니다.|  
|개체 쿼리|개체 컨텍스트 내에서 개념적 모델에 대해 실행되어 데이터를 개체로 반환하는 쿼리입니다.<br /><br /> 자세한 내용은 [개체 쿼리](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896241(v=vs.100))합니다.|  
|개체-관계형 매핑|관계형 데이터베이스의 데이터를 개체 지향 소프트웨어 응용 프로그램에서 사용할 수 있는 데이터 형식으로 변형하기 위한 기술입니다.<br /><br /> [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]는 저장소 모델에 정의된 관계형 데이터를 개념적 모델에 정의된 데이터 형식에 매핑하여 개체-관계형 매핑 서비스를 제공합니다.<br /><br /> 자세한 내용은 [모델링 및 매핑](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)합니다.|  
|개체 서비스(Object Services)|제공 하는 서비스는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] 응용 프로그램 코드를.NET Framework 개체와 같은 엔터티에서 작동할 수 있도록 합니다.|  
|지속성 무시 개체|데이터 저장소와 관련된 논리가 포함되지 않은 개체입니다. POCO 엔터티라고도 합니다.|  
|POCO|Plain Old CLR Object입니다. 다른 클래스에서 상속하거나 인터페이스를 구현하지 않는 개체입니다.|  
|POCO 엔터티|[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] 또는 <xref:System.Data.Objects.DataClasses.EntityObject>에서 상속하지 않고 <xref:System.Data.Objects.DataClasses.ComplexObject> 인터페이스를 구현하지 않는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]의 엔터티입니다. 대부분의 경우 POCO 엔터티는 기존 도메인 개체에서 사용 하는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] 응용 프로그램입니다. 이러한 엔터티는 지속성 무시를 지원합니다. 자세한 내용은 [POCO 엔터티 작업](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456853(v=vs.100))합니다.|  
|프록시 개체|POCO 클래스에서 파생되고 변경 내용 추적과 지연 로드를 지원하기 위해 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]에서 생성된 개체입니다. 자세한 내용은 [POCO 프록시 만들기에 대 한 요구 사항](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd468057(v=vs.100))합니다.|  
|참조 제약 조건(referential constraint)|엔터티와 다른 엔터티 간에 종속 관계가 있음을 나타내는, 개념적 모델에서 정의된 제약 조건입니다. 이 제약 조건은 해당하는 주 엔터티 인스턴스가 없을 경우 종속 엔터티 인스턴스가 존재할 수 없음을 의미합니다.<br /><br /> 자세한 내용은 [ReferentialConstraint 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#referentialconstraint-element-csdl) 하 고 [참조 무결성 제약 조건](../../../../../docs/framework/data/adonet/referential-integrity-constraint.md)합니다.|  
|관계|엔터티 간의 논리적 연결입니다.|  
|역할(Role)|연결의 각 `End`에 지정되어 관계의 의미 체계를 설명하는 이름입니다.<br /><br /> 자세한 내용은 [끝 요소 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#end-element-csdl) 하 고 [연결 end](../../../../../docs/framework/data/adonet/association-end.md)합니다.|  
|스칼라 속성|저장소 모델의 단일 필드에 매핑되는 엔터티의 속성입니다.|  
|자체 추적 엔터티|변경 내용을 스칼라 속성, 복합 속성 및 탐색 속성에 기록하는 기능이 있는 T4(Text Template Transformation Toolkit)에서 만들어진 엔터티입니다.|  
|단순 형식|개념적 모델에서 속성을 정의하는 데 사용되는 기본 형식입니다.<br /><br /> 자세한 내용은 [개념적 모델 형식 (CSDL)](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#conceptual-model-types-csdl) 고 [엔터티 데이터 모델: 기본 데이터 형식을](../../../../../docs/framework/data/adonet/entity-data-model-primitive-data-types.md)합니다.|  
|분할 엔터티|저장소 모델에 있는 두 개의 별도 형식에 매핑되는 엔터티 형식입니다.<br /><br /> 자세한 내용은 [방법: 두 테이블에 매핑된 단일 엔터티를 사용 하 여 모델 정의](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896233(v=vs.100))합니다.|  
|저장소 모델|관계형 데이터베이스와 같은 지원되는 데이터 소스에 있는 데이터의 논리적 모델에 대한 정의입니다. 저장소 모델은 저장소 .ssdl 파일에서 SSDL로 정의됩니다.<br /><br /> 자세한 내용은 [모델링 및 매핑](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md) 하 고 [SSDL 사양](../../../../../docs/framework/data/adonet/ef/language-reference/ssdl-specification.md)합니다.|  
|.ssdl 파일|SSDL로 표현된 저장소 모델이 포함된 XML 파일입니다.|  
|SSDL(저장소 스키마 정의 언어)|흔히 데이터베이스 스키마에 해당하는 저장소 모델의 엔터티 형식, 연결, 엔터티 컨테이너, 엔터티 집합 및 연결 집합을 정의하는 데 사용되는 XML 기반 언어입니다.<br /><br /> 자세한 내용은 [SSDL 사양](../../../../../docs/framework/data/adonet/ef/language-reference/ssdl-specification.md)합니다.|  
|계층당 하나의 테이블|형식 계층 구조를 모델링하는 방법 중 하나로, 계층 구조에 있는 모든 형식의 특성이 하나의 테이블에 포함됩니다.|  
|형식당 하나의 테이블|데이터베이스의 형식 계층 구조를 모델링하는 방법 중 하나로, 일대일 관계의 여러 테이블을 사용하여 다양한 형식을 모델링합니다.|  
  
## <a name="see-also"></a>참고자료

- [ADO.NET Entity Framework](../../../../../docs/framework/data/adonet/ef/index.md)
- [Entity Framework 개요](../../../../../docs/framework/data/adonet/ef/overview.md)
- [시작](../../../../../docs/framework/data/adonet/ef/getting-started.md)
- [Entity Framework 리소스](../../../../../docs/framework/data/adonet/ef/resources.md)
