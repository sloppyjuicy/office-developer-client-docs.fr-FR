---
title: NumericScale et Precision, propriétés – Exemple (VC++)
TOCTitle: NumericScale and Precision properties example (VC++)
ms:assetid: da4bec90-b039-1764-3b8b-c74bb725da61
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250098(v=office.15)
ms:contentKeyID: 48548078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: db4cb220e2ba29691e3aec316267692860207f89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568809"
---
# <a name="numericscale-and-precision-properties-example-vc"></a>NumericScale et Precision, propriétés – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre les propriétés [NumericScale](numericscale-property-adox.md) et [Precision](precision-property-adox.md) de l’objet [Column](column-object-adox.md). Ce code affiche leur valeur pour la table **Order Details** de la base de données *Northwind*.

```cpp 
 
// BeginNumericScalePrecCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void NumericScalePrecX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 NumericScalePrecX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// NumericScalePrecX Function // 
// // 
////////////////////////////////////////////////////////// 
void NumericScalePrecX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 _ColumnPtr m_pColumn = NULL; 
 
 //Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 //Declare string variables 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 
 // Connect the catalog. 
 m_pCnn->Open (strCnn, "", "", NULL); 
 
 m_pCatalog->PutActiveConnection(variant_t((IDispatch *)m_pCnn)); 
 
 // Retrieve the Order Details table 
 m_pTable = m_pCatalog->Tables->GetItem("Order Details"); 
 
 // Display numeric scale and precision of 
 // small integer fields. 
 _variant_t vIndex; 
 for (long lIndex=0; lIndex < m_pTable->Columns->Count; lIndex++) 
 { 
 vIndex = lIndex ; 
 m_pColumn = m_pTable->Columns->GetItem(vIndex); 
 if(m_pColumn->Type == adSmallInt) 
 { 
 cout << "Column: " << m_pColumn->GetName() << endl; 
 cout << "Numeric scale: " << (_bstr_t) m_pColumn-> 
 GetNumericScale() << endl; 
 cout << "Precision: " << m_pColumn->GetPrecision() << 
 endl; 
 } 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in NumericScalePrecX...."<< endl; 
 } 
} 
// EndNumericScalePrecCpp 
```

