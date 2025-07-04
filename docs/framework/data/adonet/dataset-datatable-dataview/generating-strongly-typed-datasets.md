---
title: 강력한 형식의 데이터 세트 생성
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 54333cbf-bb43-4314-a7d4-6dc1dd1c44b3
ms.openlocfilehash: 198d7f616d843a3c90b8d32cf33096ee253d2935
ms.sourcegitcommit: 34593b4d0be779699d38a9949d6aec11561657ec
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66832731"
---
# <a name="generating-strongly-typed-datasets"></a>강력한 형식의 데이터 세트 생성
표준 XML 스키마 정의 언어 (XSD)를 준수 하는 XML 스키마에 지정 된을 생성할 수 있습니다 강력한 형식의 <xref:System.Data.DataSet> Windows 소프트웨어 개발 키트 (SDK)으로 제공 되는 XSD.exe 도구를 사용 하 여 합니다.  
  
 (데이터베이스 테이블에서 xsd를 만들려면, 참조 <xref:System.Data.DataSet.WriteXmlSchema%2A> 나 [Visual Studio에서 데이터 집합 작업](/visualstudio/data-tools/dataset-tools-in-visual-studio)).  
  
 다음 코드를 생성 하기 위한 구문을 보여 줍니다.는 **데이터 집합** 이 도구를 사용 합니다.  
  
```  
xsd.exe /d /l:CS XSDSchemaFileName.xsd /eld /n:XSDSchema.Namespace  
```  
  
 이 구문에서은 `/d` 지시문은 생성 하는 도구를 **데이터 집합**, 및 `/l:` 도구 (예: C# 또는 Visual Basic.NET) 사용 하는 언어를 알려 줍니다. 선택적 `/eld` 지시문을 사용할 수 있는 지정 [!INCLUDE[linq_dataset](../../../../../includes/linq-dataset-md.md)] 생성 된 쿼리 **데이터 집합입니다.** 이 옵션은 `/d` 옵션도 함께 지정한 경우에 사용합니다. 자세한 내용은 [형식화 된 데이터 집합 쿼리](../../../../../docs/framework/data/adonet/querying-typed-datasets.md)합니다. 선택적 `/n:` 지시문은 또한 네임 스페이스를 생성 하는 도구를 **데이터 집합** 호출 **XSDSchema.Namespace**합니다. 이 명령을 실행하면 XSDSchemaFileName.cs가 생성되며, 이 파일을 컴파일하여 ADO.NET 응용 프로그램에서 사용할 수 있습니다. 생성된 코드는 라이브러리나 모듈로 컴파일할 수 있습니다.  
  
 다음 코드는 생성된 코드를 C# 컴파일러(csc.exe)를 사용하여 라이브러리로 컴파일하는 구문을 보여 줍니다.  
  
```  
csc.exe /t:library XSDSchemaFileName.cs /r:System.dll /r:System.Data.dll  
```  
  
 `/t:` 지시문은 도구에 라이브러리로 컴파일하라는 것을, `/r:` 지시문은 컴파일에 필요한 종속 라이브러리를 지정합니다. 이 명령을 실행하면 XSDSchemaFileName.dll이 생성되며, 이 dll은 `/r:` 지시문으로 ADO.NET 응용 프로그램을 컴파일할 때 컴파일러로 전달할 수 있습니다.  
  
 다음 코드는 ADO.NET 응용 프로그램에서 XSD.exe로 전달된 네임스페이스에 액세스하는 구문을 보여 줍니다.  
  
```vb  
Imports XSDSchema.Namespace  
```  
  
```csharp  
using XSDSchema.Namespace;  
```  
  
 다음 코드 예제에서는 형식화 된 **데이터 집합** 라는 **CustomerDataSet** 의 고객 목록을 로드 하는 **Northwind** 데이터베이스입니다. 데이터를 사용 하 여 로드 되 면를 **채우기** 메서드를 각 고객에 대해 반복 실행 합니다 **고객** 사용 하 여 형식화 된 테이블 **CustomersRow** ( **DataRow**) 개체입니다. 이에 대 한 직접 액세스를 제공 합니다 **CustomerID** 열을 통하지 합니다 **DataColumnCollection**합니다.  
  
```vb  
Dim customers As CustomerDataSet= New CustomerDataSet()  
Dim adapter As SqlDataAdapter New SqlDataAdapter( _  
  "SELECT * FROM dbo.Customers;", _  
  "Data Source=(local);Integrated " & _  
  "Security=SSPI;Initial Catalog=Northwind")  
  
adapter.Fill(customers, "Customers")  
  
Dim customerRow As CustomerDataSet.CustomersRow  
For Each customerRow In customers.Customers  
  Console.WriteLine(customerRow.CustomerID)  
Next  
```  
  
```csharp  
CustomerDataSet customers = new CustomerDataSet();  
SqlDataAdapter adapter = new SqlDataAdapter(  
  "SELECT * FROM dbo.Customers;",  
  "Data Source=(local);Integrated " +  
  "Security=SSPI;Initial Catalog=Northwind");  
  
adapter.Fill(customers, "Customers");  
  
foreach(CustomerDataSet.CustomersRow customerRow in customers.Customers)  
  Console.WriteLine(customerRow.CustomerID);  
```  
  
 다음은 예제에서 사용한 XML 스키마입니다.  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<xs:schema id="CustomerDataSet" xmlns="" xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  <xs:element name="CustomerDataSet" msdata:IsDataSet="true">  
    <xs:complexType>  
      <xs:choice maxOccurs="unbounded">  
        <xs:element name="Customers">  
          <xs:complexType>  
            <xs:sequence>  
              <xs:element name="CustomerID" type="xs:string" minOccurs="0" />  
            </xs:sequence>  
          </xs:complexType>  
        </xs:element>  
      </xs:choice>  
    </xs:complexType>  
  </xs:element>  
</xs:schema>  
```  
  
## <a name="see-also"></a>참고자료

- <xref:System.Data.DataColumnCollection>
- <xref:System.Data.DataSet>
- [형식화된 데이터 집합](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md)
- [DataSet, DataTable 및 DataView](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터](https://go.microsoft.com/fwlink/?LinkId=217917)
