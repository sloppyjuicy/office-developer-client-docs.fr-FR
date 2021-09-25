---
title: ADO NumericScale et Precision, propriétés - Exemple (VC++)
TOCTitle: NumericScale and Precision properties example (VC++)
ms:assetid: f0bc84c6-5563-509c-9b4e-3fb45c70a04e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250225(v=office.15)
ms:contentKeyID: 48548611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a2ead9ee12f51b9cffbb432787869b55f4c90202
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559275"
---
# <a name="ado-numericscale-and-precision-properties-example-vc"></a>ADO NumericScale et Precision, propriétés - Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les propriétés [NumericScale](numericscale-property-ado.md) et [Precision](precision-property-ado.md) pour afficher l’échelle numérique et la précision des champs dans la table ***Discount** _ de la base de données _ *_Pubs_** .

```cpp 
 
// BeginNumericScaleCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void NumericScaleX(void); 
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
 
 NumericScaleX(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// NumericScaleX Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void NumericScaleX(void) 
{ 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace 
 _RecordsetPtr pRstDiscounts = NULL; 
 FieldsPtr fldTemp = NULL; 
 
 //Define Other Variables 
 HRESULT hr = S_OK; 
 _variant_t Index; 
 Index.vt = VT_I2; 
 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 // Open recordset. 
 TESTHR(pRstDiscounts.CreateInstance(__uuidof(Recordset))); 
 pRstDiscounts->Open("discounts", strCnn, adOpenForwardOnly, 
 adLockReadOnly, adCmdTable); 
 
 // Display numeric scale and precision of 
 // numeric and small integer fields. 
 fldTemp = pRstDiscounts->GetFields(); 
 
 for (int intLoop=0;intLoop < (int)fldTemp->GetCount();intLoop++) 
 { 
 Index.iVal = intLoop; 
 
 if ((fldTemp->GetItem(Index)->Type == adNumeric) 
 || (fldTemp->GetItem(Index)->Type == adSmallInt)) 
 { 
 printf("Field: %s\n" ,(LPCSTR)fldTemp-> 
 GetItem(Index)->GetName()); 
 printf("Numeric scale: %d\n", fldTemp-> 
 GetItem(Index)->GetNumericScale()); 
 printf("Precision: %d\n", fldTemp-> 
 GetItem(Index)->GetPrecision()); 
 } 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstDiscounts->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
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
 if (pRstDiscounts) 
 if (pRstDiscounts->State == adStateOpen) 
 pRstDiscounts->Close(); 
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
 for(long i = 0;i < nCount;i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("\t Error number: %x\t%s", pErr->Number, 
 pErr->Description); 
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
 
 // Print COM errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
// EndNumericScaleCpp 
```

