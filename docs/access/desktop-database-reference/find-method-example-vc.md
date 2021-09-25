---
title: Find, méthode – Exemple (VC++)
TOCTitle: Find method example (VC++)
ms:assetid: dc6adb54-48ef-475e-7b52-435ac0fc63ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250114(v=office.15)
ms:contentKeyID: 48548137
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dfb6bd3e78efc6601aa93beffb13d11d8e68db00
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565288"
---
# <a name="find-method-example-vc"></a>Find, méthode – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la méthode [Find](find-method-ado.md) de l’objet [Recordset](recordset-object-ado.md) pour localiser et compter le nombre de titres de fonctions dans la base de données ***Pubs***. Il est supposé, dans l'exemple, que le fournisseur sous-jacent ne prend pas en charge de fonctionnalité similaire.

```cpp 
 
// BeginFindCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
#include "FindX.h" 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void FindX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
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
 
 FindX(); 
 
 //Wait here for the user to see the output. 
 printf("Press any key to continue..."); 
 getch(); 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// FindX Function // 
// // 
////////////////////////////////////////////////////////// 
 
void FindX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 _RecordsetPtr pRstTitles = NULL; 
 IADORecordBinding *picRs = NULL; //Interface Pointer declared. 
 CTitlesRs titlers; //C++ class object 
 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 // Open connection. 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 
 // Open title Table 
 TESTHR(pRstTitles.CreateInstance(__uuidof(Recordset))); 
 
 pRstTitles->Open("SELECT title_id FROM titles", 
 _variant_t((IDispatch *)pConnection), 
 adOpenStatic, adLockReadOnly, adCmdText); 
 
 // The default parameters are sufficient to search forward 
 // through a Recordset. 
 
 pRstTitles->Find ("title_id LIKE 'BU%'",0,adSearchForward,""); 
 
 //Open an IADORecordBinding interface pointer which 
 //we'll use for Binding Recordset to a class 
 TESTHR(pRstTitles->QueryInterface( 
 __uuidof(IADORecordBinding),(LPVOID*)&picRs)); 
 
 //Bind the Recordset to a C++ Class here 
 TESTHR(picRs->BindToRecordset(&titlers)); 
 
 // Skip the current record to avoid finding the same 
 // row repeatedly. The bookmark is redundant because Find 
 // searches from the current position. 
 int count = 0; 
 
 //Continue if last find succeeded. 
 while (!(pRstTitles->EndOfFile)) 
 { 
 printf("Title ID: %s\n",titlers.lt_titleidStatus == adFldOK ? 
 titlers.m_szt_titleid : "<NULL>"); 
 count++; //Count the last title found. 
 
 _variant_t mark = pRstTitles->Bookmark; //Note current pos. 
 pRstTitles->Find("title_id LIKE 'BU%'", 1, adSearchForward, 
 mark); 
 } 
 printf("The number of business titles is %d\n",count); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 //Release the IADORecordset Interface here 
 if (picRs) 
 picRs->Release(); 
 
 if (pRstTitles) 
 if (pRstTitles->State == adStateOpen) 
 pRstTitles->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
////////////////////////////////////////////////////////// 
 
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
 printf("\t Error number: %x\t%s", pErr->Number, 
 (LPCSTR)pErr->Description); 
 } 
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
// EndFindCpp 
```

**FindX.h**

```cpp 
 
// BeginFindH 
#include "icrsint.h" 
 
//This Class extracts only titleId from Titles table. 
class CTitlesRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CTitlesRs) 
 
 // Column title_id is the 1st field in the recordset 
 // from Titles table. 
 ADO_VARIABLE_LENGTH_ENTRY2(1, adVarChar, m_szt_titleid, 
 sizeof(m_szt_titleid), lt_titleidStatus, FALSE) 
 
END_ADO_BINDING() 
 
public: 
 CHAR m_szt_titleid[150]; 
 ULONG lt_titleidStatus; 
}; 
// EndFindH 
```

