---
title: CursorType, LockType et EditMode, propriétés – Exemple (VC++)
TOCTitle: CursorType, LockType, and EditMode properties example (VC++)
ms:assetid: edbc4625-5013-cfcd-d709-ac8a85fe17b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250205(v=office.15)
ms:contentKeyID: 48548545
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 92443742ad45f5fb16d210cdcc7ad45f3aa4c33a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558561"
---
# <a name="cursortype-locktype-and-editmode-properties-example-vc"></a>CursorType, LockType et EditMode, propriétés – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la définition des propriétés [CursorType](cursortype-property-ado.md) et [LockType](locktype-property-ado.md) avant l’ouverture d’un objet [Recordset](recordset-object-ado.md). Il indique également la valeur de la propriété [EditMode](editmode-property-ado.md) dans différentes conditions. La fonction EditModeOutput est nécessaire à l’exécution de cette procédure.

```cpp 
 
// BeginEditModeCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declaration 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void EditModeX(void); 
void EditModeOutput(char *, int); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
/////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 EditModeX(); 
 
 // Wait here for the user to see the output 
 printf("\n\nPress any key to continue..."); 
 getch(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// EditModeX Function // 
// // 
/////////////////////////////////////////////////////////// 
void EditModeX(void) 
{ 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstEmployees = NULL; 
 _ConnectionPtr pConnection = NULL; 
 
 HRESULT hr = S_OK; 
 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 // Open a connection 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 hr = pConnection->Open(strCnn,"","",adConnectUnspecified); 
 
 // Open recordset with data from employee table 
 TESTHR(pRstEmployees.CreateInstance(__uuidof(Recordset))); 
 
 pRstEmployees->CursorLocation = adUseClient; 
 pRstEmployees->CursorType = adOpenStatic; 
 pRstEmployees->LockType = adLockBatchOptimistic; 
 
 pRstEmployees->Open("employee", 
 _variant_t((IDispatch *) pConnection,true), 
 adOpenStatic,adLockBatchOptimistic,adCmdTable); 
 
 // Show the EditMode property under different editing states. 
 pRstEmployees->AddNew (); 
 pRstEmployees->Fields->Item["emp_id"]->Value = 
 (_bstr_t)("T-T55555M"); 
 pRstEmployees->Fields->Item["fname"]->Value = 
 (_bstr_t)("temp_fname"); 
 pRstEmployees->Fields->Item["lname"]->Value = 
 (_bstr_t)("temp_lname"); 
 EditModeOutput("After AddNew: ", pRstEmployees->EditMode); 
 
 pRstEmployees->UpdateBatch(adAffectCurrent); 
 EditModeOutput("After Update: ", pRstEmployees->EditMode); 
 
 pRstEmployees->Fields->Item["fname"]->Value = (_bstr_t)("test"); 
 EditModeOutput("After Edit: ", pRstEmployees->EditMode); 
 
 // Delete new record because this is a demonstration. 
 pConnection->Execute("DELETE FROM employee WHERE emp_id = " 
 "'T-T55555M'", NULL, adCmdText); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRstEmployees) 
 if (pRstEmployees->State == adStateOpen) 
 pRstEmployees->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// EditModeOutput() Function // 
// // 
/////////////////////////////////////////////////////////// 
void EditModeOutput(char *strTemp, int intEditMode) 
{ 
 // Print report based on the value of the EditMode property. 
 printf("\n%s", strTemp); 
 printf("\n EditMode = "); 
 
 switch (intEditMode) 
 { 
 case adEditNone : 
 printf("adEditNone"); 
 break; 
 case adEditInProgress : 
 printf("adEditInProgress"); 
 break; 
 case adEditAdd : 
 printf("adEditAdd"); 
 break; 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0; i < nCount; i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("\n\t Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR)pErr->Description); 
 } 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void PrintComError(_com_error &e) 
{ 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print Com errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
 
// EndEditModeCpp 
```

