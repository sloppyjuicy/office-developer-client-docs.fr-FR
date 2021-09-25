---
title: Command et CommandText, propriétés – Exemple (VC++)
TOCTitle: Command and CommandText properties example (VC++)
ms:assetid: 99eac61e-22fe-0e2c-542a-7f6ad14f3d60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249692(v=office.15)
ms:contentKeyID: 48546525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 581a67549c04599ee4995315d34bd36b1b2202c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573109"
---
# <a name="command-and-commandtext-properties-example-vc"></a>Command et CommandText, propriétés – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) pour mettre à jour le texte d'une procédure.

```cpp 
 
// BeginCommandTextCpp 
// This sample runs correctly only if procedure 'CustomerById' 
// exists. If the procedure doesn't exist, please use 
// 'ADOXProceduresAppend.cpp' to creat it. 
 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ProcedureTextX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ProcedureTextX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// ProcedureTextX Function // 
// // 
////////////////////////////////////////////////////////// 
void ProcedureTextX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 
 // Define ADODB object pointers. 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 ADODB::_CommandPtr m_pCommand = NULL; 
 
 try 
 { 
 //Open the Connection 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 TESTHR(hr = m_pCommand.CreateInstance(__uuidof(ADODB::Command))); 
 m_pCnn->Open("Provider='Microsoft.JET.OLEDB.4.0';" 
 "data source='c:\\Program Files\\Microsoft Office" 
 "\\Office\\Samples\\Northwind.mdb';","","",NULL); 
 
 // Open the catalog 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 // Get the Command 
 m_pCommand = m_pCatalog->Procedures->GetItem("CustomerById")->GetCommand(); 
 
 // Update the CommandText 
 m_pCommand->PutCommandText("PARAMETERS [CustId] Text;select " 
 "CustomerId, CompanyName, ContactName " 
 "from Customers where CustomerId = [CustId]"); 
 printf("CommandText is updated.\n"); 
 
 // Update the Procedure 
 m_pCatalog->Procedures->GetItem("CustomerById")->PutCommand( 
 _variant_t((IDispatch *)m_pCommand)); 
 printf("Procedure 'CustomerById' is updated.\n"); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ",(LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in ProcedureTextX...."<< endl; 
 } 
} 
// EndCommandTextCpp 
```

