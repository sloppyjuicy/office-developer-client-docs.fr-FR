---
title: Save et Open, méthodes – Exemple (VC++)
TOCTitle: Save and Open methods example (VC++)
ms:assetid: 83e9647e-5dbd-2c59-4fff-2a3df79ab93c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249574(v=office.15)
ms:contentKeyID: 48546019
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 16fcea9411d846ed793ce80c6a238407178917ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626098"
---
# <a name="save-and-open-methods-example-vc"></a>Save et Open, méthodes – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Ces trois exemples montrent comment utiliser conjointement les méthodes [Save](save-method-ado.md) et **Open**.

Supposons que vous partez en voyage d'affaires et que vous souhaitez emporter une table de la base de données. Avant de partir, vous accédez aux données sous la forme d'un objet [Recordset](recordset-object-ado.md) et vous l'enregistrez dans un format transportable. Lorsque vous arrivez à destination, vous accédez à l'objet **Recordset** en tant qu'objet **Recordset** déconnecté, local. Vous modifiez l'objet **Recordset** avant de le réenregistrer. Enfin, un fois de retour, vous vous reconnectez à la base de données et vous la mettez à jour avec les modifications apportées au cours de votre voyage.

```cpp 
 
// BeginSaveCpp 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
#include <io.h> 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
bool FileExists(void); 
void SaveX1(void); 
void SaveX2(void); 
void SaveX3(void); 
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
 
 //If File exists in the specified directory, then display error 
 if (!FileExists()) 
 { 
 SaveX1(); 
 SaveX2(); 
 SaveX3(); 
 } 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SaveX1 Function // 
// // 
////////////////////////////////////////////////////////// 
 
//First, access and save the authors table. 
void SaveX1() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstAuthors = NULL; 
 
 //Definitions of other variables 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 pRstAuthors->Open("SELECT * FROM authors",strCnn, 
 adOpenDynamic,adLockBatchOptimistic,adCmdText); 
 
 // For sake of illustration, save the Recordset to a diskette 
 // in XML format. 
 pRstAuthors->Save("c:\\pubs.xml",adPersistXML); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstAuthors->GetActiveConnection(); 
 
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
 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SaveX2 Function // 
// // 
////////////////////////////////////////////////////////// 
//At this point, you have arrived at your destination. 
//You will access the authors table as a local, disconnected Recordset. 
//Don't forget you must have the MSPersist provider on the machine you 
//are using in order to access the saved file, c:\pubs.xml. 
void SaveX2() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstAuthors = NULL; 
 
 try 
 { 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 //For sake of illustration, we specify all parameters. 
 pRstAuthors->Open("c:\\pubs.xml","Provider='MSPersist';", 
 adOpenForwardOnly,adLockBatchOptimistic,adCmdFile); 
 
 //Now you have a local, disconnected Recordset. 
 //Edit it as you desire. 
 //(In this example, the change makes no difference). 
 pRstAuthors->Find("au_lname = 'Carson'",NULL,adSearchForward); 
 if (pRstAuthors->EndOfFile) 
 { 
 printf("Name not found ...\n"); 
 pRstAuthors->Close(); 
 return; 
 } 
 pRstAuthors->GetFields()->GetItem("City")->PutValue("Chicago"); 
 pRstAuthors->Update(); 
 
 // Save changes in ADTG format this time, purely for sake of 
 // illustration. Note that the previous version is still on the 
 // diskette as c:\pubs.xml. 
 pRstAuthors->Save("c:\\pubs.adtg",adPersistADTG); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstAuthors->GetActiveConnection(); 
 
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
 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SaveX3 Function // 
// // 
////////////////////////////////////////////////////////// 
//Finally, you return home. Now update the database with 
//your changes. 
void SaveX3() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstAuthors = NULL; 
 _ConnectionPtr pCnn = NULL; 
 
 //Definitions of other variables 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 TESTHR(pCnn.CreateInstance(__uuidof(Connection))); 
 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 //If there is no ActiveConnection, you can open with defaults. 
 pRstAuthors->Open("c:\\pubs.adtg","Provider=MSPersist;", 
 adOpenForwardOnly,adLockBatchOptimistic,adCmdFile); 
 
 //Connect to the database, associate the Recordset with 
 //the connection, then update the database table with the 
 //changed Recordset. 
 pCnn->Open(strCnn,"","",NULL); 
 
 pRstAuthors->PutActiveConnection(_variant_t((IDispatch *) pCnn)); 
 pRstAuthors->UpdateBatch(adAffectAll); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstAuthors->GetActiveConnection(); 
 
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
 
 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
 if (pCnn) 
 if (pCnn->State == adStateOpen) 
 pCnn->Close(); 
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
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
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
 
bool FileExists() 
{ 
 struct _finddata_t xml_file; 
 long hFile; 
 
 if( (hFile = _findfirst("c:\\pubs.xml", &xml_file )) != -1L) 
 { 
 printf( "File already exists!\n" ); 
 return(true); 
 } 
 else 
 return (false); 
} 
// EndSaveCpp 
```

