---
<span data-ttu-id="23027-101"><<<<<<< Titre tête : Command et CommandText, propriétés-exemple (VC ++) TOCTitle : commande et CommandText, propriétés-exemple (VC ++) === titre : Command et CommandText, propriétés-exemple (VC ++) TOCTitle : Command et CommandText propriétés-exemple (VC ++)</span><span class="sxs-lookup"><span data-stu-id="23027-101"><<<<<<< HEAD title: Command and CommandText Properties Example (VC++) TOCTitle: Command and CommandText Properties Example (VC++) ======= title: Command and CommandText properties example (VC++) TOCTitle: Command and CommandText properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="23027-102">Master ms:assetid : 99eac61e-22fe-0e2c-542a-7f6ad14f3d60 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249692(v=office.15) ms:contentKeyID : ms.date 48546525 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="23027-102">master ms:assetid: 99eac61e-22fe-0e2c-542a-7f6ad14f3d60 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249692(v=office.15) ms:contentKeyID: 48546525 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="23027-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="23027-103"><<<<<<< HEAD</span></span>
# <a name="command-and-commandtext-properties-example-vc"></a><span data-ttu-id="23027-104">Command et CommandText, propriétés - Exemple (VC++)</span><span class="sxs-lookup"><span data-stu-id="23027-104">Command and CommandText Properties Example (VC++)</span></span>
=======
# <a name="command-and-commandtext-properties-example-vc"></a><span data-ttu-id="23027-105">Command et CommandText, propriétés-exemple (VC ++)</span><span class="sxs-lookup"><span data-stu-id="23027-105">Command and CommandText properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="23027-106">master</span><span class="sxs-lookup"><span data-stu-id="23027-106">master</span></span>


<span data-ttu-id="23027-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="23027-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23027-108">Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) pour mettre à jour le texte d'une procédure.</span><span class="sxs-lookup"><span data-stu-id="23027-108">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a procedure.</span></span>

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

