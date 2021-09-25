---
title: Type, propriété – Exemple (Property) (VC++)
TOCTitle: Type property example (Property) (VC++)
ms:assetid: ddf0233f-585e-6659-7fd6-f924f3a31f21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250122(v=office.15)
ms:contentKeyID: 48548168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dbebfce5371b7e7b4295542d2c893b08bb07ad6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564784"
---
# <a name="type-property-example-property-vc"></a>Type, propriété – Exemple (Property) (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la propriété [Type](type-property-ado.md). C'est un modèle d'utilitaire permettant de répertorier les noms et les types d'une collection ([Properties](properties-collection-ado.md) ou [Fields](fields-collection-ado.md), par exemple).

Il n'est pas nécessaire d'ouvrir le [Recordset](recordset-object-ado.md) pour accéder à la collection **Properties** qui lui correspond ; ses propriétés sont générées lorsque l'objet **Recordset** est instancié. Toutefois, si l'on attribue à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, cela ajoute plusieurs propriétés dynamiques à la collection **Properties** de l'objet **Recordset**, ce qui rend l'exemple un peu plus intéressant. Pour les besoins de l'illustration, nous utilisons explicitement la propriété [Item](item-property-ado.md) pour accéder à chaque objet [Property](property-object-ado.md).

```cpp 
 
// BeginTypePropertyCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include<conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void TypeX(); 
void PrintComError(_com_error &e); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 TypeX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// TypeX Function // 
// // 
////////////////////////////////////////////////////////// 
void TypeX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace 
 _RecordsetPtr pRst = NULL; 
 PropertyPtr pProperty = NULL; 
 
 //Define Other Variables 
 _bstr_t strMsg; 
 _variant_t vIndex; 
 int intLineCnt = 0; 
 
 try 
 { 
 TESTHR(pRst.CreateInstance (__uuidof(Recordset))); 
 
 // Set the Recordset Cursor Location 
 pRst->CursorLocation = adUseClient; 
 
 for (short iIndex = 0; iIndex <= (pRst->Properties-> 
 GetCount() - 1);iIndex++) 
 { 
 vIndex = iIndex; 
 pProperty = pRst->Properties->GetItem(vIndex); 
 
 int propType = (int)pProperty->GetType(); 
 switch(propType) 
 { 
 case adBigInt: 
 strMsg = "adBigInt"; 
 break; 
 case adBinary: 
 strMsg = "adBinary"; 
 break; 
 case adBoolean: 
 strMsg = "adBoolean"; 
 break; 
 case adBSTR: 
 strMsg = "adBSTR"; 
 break; 
 case adChapter: 
 strMsg = "adChapter"; 
 break; 
 case adChar: 
 strMsg = "adChar"; 
 break; 
 case adCurrency: 
 strMsg = "adCurrency"; 
 break; 
 case adDate: 
 strMsg = "adDate"; 
 break; 
 case adDBDate: 
 strMsg = "adDBDate"; 
 break; 
 case adDBTime: 
 strMsg = "adDBTime"; 
 break; 
 case adDBTimeStamp: 
 strMsg = "adDBTimeStamp"; 
 break; 
 case adDecimal: 
 strMsg = "adDecimal"; 
 break; 
 case adDouble: 
 strMsg = "adDouble"; 
 break; 
 case adEmpty: 
 strMsg = "adEmpty"; 
 break; 
 case adError: 
 strMsg = "adError"; 
 break; 
 case adFileTime: 
 strMsg = "adFileTime"; 
 break; 
 case adGUID: 
 strMsg = "adGUID"; 
 break; 
 case adIDispatch: 
 strMsg = "adIDispatch"; 
 break; 
 case adInteger: 
 strMsg = "adInteger"; 
 break; 
 case adIUnknown: 
 strMsg = "adIUnknown"; 
 break; 
 case adLongVarBinary: 
 strMsg = "adLongVarBinary"; 
 break; 
 case adLongVarChar: 
 strMsg = "adLongVarChar"; 
 break; 
 case adLongVarWChar: 
 strMsg = "adLongVarWChar"; 
 break; 
 case adNumeric: 
 strMsg = "adNumeric"; 
 break; 
 case adPropVariant: 
 strMsg = "adPropVariant"; 
 break; 
 case adSingle: 
 strMsg = "adSingle"; 
 break; 
 case adSmallInt: 
 strMsg = "adSmallInt"; 
 break; 
 case adTinyInt: 
 strMsg = "adTinyInt"; 
 break; 
 case adUnsignedBigInt: 
 strMsg = "adUnsignedBigInt"; 
 break; 
 case adUnsignedInt: 
 strMsg = "adUnsignedInt"; 
 break; 
 case adUnsignedSmallInt: 
 strMsg = "adUnsignedSmallInt"; 
 break; 
 case adUnsignedTinyInt: 
 strMsg = "adUnsignedTinyInt"; 
 break; 
 case adUserDefined: 
 strMsg = "adUserDefined"; 
 break; 
 case adVarBinary: 
 strMsg = "adVarBinary"; 
 break; 
 case adVarChar: 
 strMsg = "adVarChar"; 
 break; 
 case adVariant: 
 strMsg = "adVariant"; 
 break; 
 case adVarNumeric: 
 strMsg = "adVarNumeric"; 
 break; 
 case adVarWChar: 
 strMsg = "adVarWChar"; 
 break; 
 case adWChar: 
 strMsg = "adWChar"; 
 break; 
 default: 
 strMsg = "*UNKNOWN*"; 
 break; 
 } 
 
 intLineCnt++; 
 if (intLineCnt%20 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 printf ("Property %d : %s,Type = %s\n",iIndex, 
 (LPCSTR)pProperty->GetName(),(LPCSTR)strMsg); 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintComError(e); 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
////////////////////////////////////////////////////////// 
 
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
// EndTypePropertyCpp 
```

