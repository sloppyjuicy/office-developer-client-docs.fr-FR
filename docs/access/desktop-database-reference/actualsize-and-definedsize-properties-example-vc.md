---
title: ActualSize et DefinedSize, propriétés – Exemple (VC++)
TOCTitle: ActualSize and DefinedSize properties example (VC++)
ms:assetid: 90b7a53f-c9b1-f3c1-f769-e6a340c90eba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249638(v=office.15)
ms:contentKeyID: 48546328
ms.date: 10/16/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a0a26ba7a428b5b681052657240a300cbef4b8d7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569495"
---
# <a name="actualsize-and-definedsize-properties-example-vc"></a>ActualSize et DefinedSize, propriétés – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [ActualSize](actualsize-property-ado.md) et [DefinedSize](definedsize-property-ado.md) pour afficher la taille définie et la taille réelle d'un champ.

```cpp 
 
// BeginActualSizeCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ActualSizeX(VOID); 
void PrintProviderError(_ConnectionPtr pConnection); 
 
/////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 ActualSizeX(); 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// ActualSizeX Function // 
// // 
/////////////////////////////////////////////////////////// 
VOID ActualSizeX(VOID) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstStores = NULL; 
 
 //Define Other variables 
 _bstr_t strMessage; 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 //Open a recordset for the stores table. 
 TESTHR(pRstStores.CreateInstance(__uuidof(Recordset))); 
 
 //You have to explicitly pass the Cursor type and LockType 
 //to the Recordset here. 
 hr = pRstStores->Open("stores", 
 strCnn,adOpenForwardOnly,adLockReadOnly,adCmdTable); 
 
 //Loop through the recordset displaying the contents 
 //of the stor_name field, the field's defined size, 
 //and its actual size. 
 
 pRstStores->MoveFirst(); 
 
 while(!(pRstStores->EndOfFile)) 
 { 
 strMessage = "Store Name: "; 
 strMessage += (_bstr_t)pRstStores->Fields-> 
 Item["stor_name"]->Value + "\n"; 
 strMessage += "Defined Size: "; 
 strMessage += (_bstr_t)pRstStores->Fields-> 
 Item["stor_name"]->DefinedSize + "\n"; 
 strMessage += "Actual Size: "; 
 strMessage += (_bstr_t) pRstStores->Fields-> 
 Item["stor_name"]->ActualSize + "\n"; 
 
 printf("%s\n",(LPCSTR)strMessage); 
 printf("Press any key to continue..."); 
 getch(); 
 //Clear the screen for the next display 
 system("cls"); 
 pRstStores->MoveNext(); 
 } 
 } 
 catch(_com_error &e) 
 { 
 _variant_t vtConnect = pRstStores->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Message = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 break; 
 case VT_DISPATCH: 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 
 // Clean up objects before exit. 
 if (pRstStores) 
 if (pRstStores->State == adStateOpen) 
 pRstStores->Close(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
VOID PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 long nCount = 0; 
 long i = 0; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 nCount = pConnection->Errors->Count; 
 // Collection ranges from 0 to nCount -1. 
 for(i = 0; i < nCount; i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("\t Error number: %x\t%s", pErr->Number,(LPCSTR ) pErr->Description); 
 } 
 } 
} 
// EndActualSizeCpp 
```

