---
<span data-ttu-id="e5ac5-101"><<<<<<< Titre tête : Parameters, Collection, exemple de propriété Command (VC ++) TOCTitle : Parameters, Collection de commande, propriété-Exemple (VC ++) === titre : Parameters, Collection, exemple de propriété Command (VC ++) TOCTitle : Parameters, Collection, exemple de propriété Command (VC ++)</span><span class="sxs-lookup"><span data-stu-id="e5ac5-101"><<<<<<< HEAD title: Parameters Collection, Command Property Example (VC++) TOCTitle: Parameters Collection, Command Property Example (VC++) ======= title: Parameters Collection, Command property example (VC++) TOCTitle: Parameters Collection, Command property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="e5ac5-102">Master ms:assetid : 625a83d5-5b73-f945-7e01-bf412fed0827 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249369(v=office.15) ms:contentKeyID : ms.date 48545237 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="e5ac5-102">master ms:assetid: 625a83d5-5b73-f945-7e01-bf412fed0827 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249369(v=office.15) ms:contentKeyID: 48545237 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e5ac5-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="e5ac5-103"><<<<<<< HEAD</span></span>
# <a name="parameters-collection-command-property-example-vc"></a><span data-ttu-id="e5ac5-104">Parameters, collection - Exemple de propriété Command (VC++)</span><span class="sxs-lookup"><span data-stu-id="e5ac5-104">Parameters Collection, Command Property Example (VC++)</span></span>
=======
# <a name="parameters-collection-command-property-example-vc"></a><span data-ttu-id="e5ac5-105">Parameters, Collection, exemple de propriété Command (VC ++)</span><span class="sxs-lookup"><span data-stu-id="e5ac5-105">Parameters Collection, Command property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="e5ac5-106">master</span><span class="sxs-lookup"><span data-stu-id="e5ac5-106">master</span></span>


<span data-ttu-id="e5ac5-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5ac5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e5ac5-108">Le code suivant montre comment utiliser la propriété [Command](command-property-adox.md) avec l'objet [Command](command-object-ado.md) afin d'extraire les données de paramètres pour la procédure.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-108">The following code demonstrates how to use the [Command](command-property-adox.md) property with the [Command](command-object-ado.md) object to retrieve parameter information for the procedure.</span></span>

```cpp 
 
// This sample runs correctly only if procedure 'CustomerById' 
// exists. If the procedure doesn't exist, please use 
// 'ADOXProceduresAppend.cpp' to creat it. 
 
// BeginProcedureParametersCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ProcedureParametersX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ProcedureParametersX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// ProcedureParametersX Function // 
// // 
////////////////////////////////////////////////////////// 
void ProcedureParametersX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 
 //Define ADODB object pointers. 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 ADODB::_CommandPtr m_pCommand = NULL; 
 ADODB::_ParameterPtr m_pParameter = NULL; 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 //Open the Connection 
 m_pCnn->Open("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';","","",NULL); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 //Open the catalog 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 //Get the command object 
 m_pCommand = m_pCatalog->Procedures->GetItem("CustomerById")-> 
 GetCommand(); 
 
 _variant_t vIndex; 
 
 //Retrieve Parameter information 
 m_pCommand->Parameters->Refresh(); 
 for (long lIndex = 0; lIndex < m_pCommand->Parameters->Count; 
 lIndex ++) 
 { 
 vIndex = lIndex; 
 m_pParameter = m_pCommand->Parameters->GetItem(vIndex); 
 cout << m_pParameter->Name << ":" << m_pParameter->Type << 
 "\n" << endl; 
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
 cout << "Error occured in ProcedureParametersX...."<< endl; 
 } 
} 
// EndProcedureParametersCpp 
```

