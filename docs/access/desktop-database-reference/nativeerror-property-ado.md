---
<span data-ttu-id="7f0ee-101"><<<<<<< Titre tête : TOCTitle NativeError propriété (ADO) : NativeError propriété (ADO) === titre : NativeError, propriété (ADO) TOCTitle : NativeError, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f0ee-101"><<<<<<< HEAD title: NativeError Property (ADO) TOCTitle: NativeError Property (ADO) ======= title: NativeError property (ADO) TOCTitle: NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="7f0ee-102">Master ms:assetid : 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl : https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID : ms.date 48546685 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="7f0ee-102">master ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="7f0ee-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="7f0ee-103"><<<<<<< HEAD</span></span>
# <a name="nativeerror-property-ado"></a><span data-ttu-id="7f0ee-104">NativeError, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f0ee-104">NativeError Property (ADO)</span></span>
=======
# <a name="nativeerror-property-ado"></a><span data-ttu-id="7f0ee-105">NativeError, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f0ee-105">NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="7f0ee-106">master</span><span class="sxs-lookup"><span data-stu-id="7f0ee-106">master</span></span>


<span data-ttu-id="7f0ee-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f0ee-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f0ee-108">Indique le code d'erreur spécifique au fournisseur pour un objet [Error](error-object-ado.md) donné.</span><span class="sxs-lookup"><span data-stu-id="7f0ee-108">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="7f0ee-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="7f0ee-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="7f0ee-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f0ee-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="7f0ee-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f0ee-111">Return value</span></span>
>>>>>>> <span data-ttu-id="7f0ee-112">master</span><span class="sxs-lookup"><span data-stu-id="7f0ee-112">master</span></span>

<span data-ttu-id="7f0ee-113">Renvoie une valeur de type **Long** qui indique le code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="7f0ee-113">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f0ee-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f0ee-114">Remarks</span></span>

<span data-ttu-id="7f0ee-p101">Utilisez la propriété **NativeError** pour récupérer les informations spécifiques à la base de données sur l'objet **Error** concerné. Par exemple, lorsque l'on utilise un fournisseur Microsoft ODBC pour OLE DB avec une base de données Microsoft SQL, les codes d'erreur d'origine provenant de SQL Server transitent par ODBC et par le fournisseur ODBC pour atteindre la propriété **Native Error** ADO.</span><span class="sxs-lookup"><span data-stu-id="7f0ee-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

