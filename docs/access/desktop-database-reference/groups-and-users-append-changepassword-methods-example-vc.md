---
title: Groups Append, Users Append, ChangePassword, méthodes – Exemple (VC++)
TOCTitle: Groups and Users Append, ChangePassword methods example (VC++)
ms:assetid: 4eaaed4f-f5bf-38d0-b984-8e3f344923c5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249252(v=office.15)
ms:contentKeyID: 48544759
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5fcff80573e37caed0ae408b16e787ef488273e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594222"
---
# <a name="groups-and-users-append-changepassword-methods-example-vc"></a>Groups Append, Users Append, ChangePassword, méthodes – Exemple (VC++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre la méthode [Append](append-method-adox-groups.md) de la collection [Groups](groups-collection-adox.md), ainsi que la méthode [Append](append-method-adox-users.md) de la collection [Users](users-collection-adox.md) en ajoutant un nouvel objet [Group](group-object-adox.md) et un nouvel objet [User](user-object-adox.md) au système. Le nouvel objet **Group** est ajouté à la collection **Groups** du nouvel objet **User**. Par conséquent, le nouvel objet **User** est ajouté à l'objet **Group**. Par ailleurs, la méthode [ChangePassword](changepassword-method-adox.md) est utilisée pour spécifier le mot de passe de l'objet **User**.

```cpp 
 
// BeginGroupCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
void GroupX(void); 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 GroupX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// GroupX Function // 
// // 
////////////////////////////////////////////////////////// 
void GroupX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _UserPtr m_pUserNew = NULL; 
 _UserPtr m_pUser = NULL; 
 _GroupPtr m_pGroup = NULL; 
 
 // Define String Variables. 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data source = 'c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';" 
 "jet oledb:system database='c:\\Program Files\\Microsoft Office\\" 
 "Office\\system.mdw'"); 
 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 m_pCatalog->PutActiveConnection(strCnn); 
 
 // Create and append new group with a string. 
 m_pCatalog->Groups->Append("Accounting"); 
 
 // Create and append new user with an object. 
 TESTHR(hr = m_pUserNew.CreateInstance(__uuidof(User))); 
 m_pUserNew->PutName("Pat Smith"); 
 m_pUserNew->ChangePassword("","Password1"); 
 m_pCatalog->Users->Append( 
 _variant_t((IDispatch *)m_pUserNew),""); 
 
 // Make the user Pat Smith a member of the 
 // Accounting group by creating and adding the 
 // appropriate Group object to the user's Groups 
 // collection.The same is accomplished if a User 
 // object representing Pat Smith is created and 
 // appended to the Accounting group Users collection 
 m_pUserNew->Groups->Append("Accounting"); 
 
 // Enumerate all User objects in the 
 // catalog's Users collection. 
 long lUsrIndex; 
 long lGrpIndex; 
 _variant_t vIndex; 
 for (lUsrIndex=0; lUsrIndex<m_pCatalog->Users->Count; lUsrIndex++) 
 { 
 vIndex = lUsrIndex; 
 m_pUser = m_pCatalog->Users->GetItem(vIndex); 
 cout<<" "<<m_pUser->Name <<endl; 
 cout<<" Belongs to these groups:"<<endl; 
 
 // Enumerate all Group objects in each User 
 // object's Groups collection. 
 if(m_pUser->Groups->Count != 0) 
 { 
 for(lGrpIndex=0;lGrpIndex<m_pUser->Groups->Count;lGrpIndex++) 
 { 
 vIndex = lGrpIndex; 
 m_pGroup = m_pUser->Groups->GetItem(vIndex); 
 cout<<" "<< m_pGroup->Name<<endl; 
 } 
 } 
 else 
 cout<<" [None]"<<endl; 
 } 
 
 // Enumerate all Group objects in the default 
 // workspace's Groups collection. 
 for (lGrpIndex=0; lGrpIndex<m_pCatalog->Groups->Count; lGrpIndex++) 
 { 
 vIndex = lGrpIndex; 
 m_pGroup = m_pCatalog->Groups->GetItem(vIndex); 
 cout<<" "<< m_pGroup->Name <<endl; 
 cout<<" Has as its members:"<<endl; 
 
 // Enumerate all User objects in each Group 
 // object's Users Collection. 
 if(m_pGroup->Users->Count != 0) 
 { 
 for (lUsrIndex=0; lUsrIndex<m_pGroup->Users->Count; lUsrIndex++) 
 { 
 vIndex = lUsrIndex; 
 m_pUser = m_pGroup->Users->GetItem(vIndex); 
 cout<<" "<<m_pUser->Name<<endl; 
 } 
 } 
 else 
 cout<<" [None]"<<endl; 
 } 
 
 // Delete new User and Group object because this 
 // is only a demonstration. 
 m_pCatalog->Users->Delete("Pat Smith"); 
 m_pCatalog->Groups->Delete("Accounting"); 
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
 cout << "Error occured in include files...."<< endl; 
 } 
} 
// EndGroupCpp 
```

