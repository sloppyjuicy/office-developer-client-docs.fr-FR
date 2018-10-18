---
<span data-ttu-id="faaf4-101"><<<<<<< Titre tête : TOCTitle nombre propriété (ADO) : numéro de propriété (ADO) === titre : Number, propriété (ADO) TOCTitle : Number, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="faaf4-101"><<<<<<< HEAD title: Number Property (ADO) TOCTitle: Number Property (ADO) ======= title: Number property (ADO) TOCTitle: Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="faaf4-102">Master ms:assetid : b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID : ms.date 48547243 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="faaf4-102">master ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="faaf4-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="faaf4-103"><<<<<<< HEAD</span></span>
# <a name="number-property-ado"></a><span data-ttu-id="faaf4-104">Number, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="faaf4-104">Number Property (ADO)</span></span>
=======
# <a name="number-property-ado"></a><span data-ttu-id="faaf4-105">Number, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="faaf4-105">Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="faaf4-106">master</span><span class="sxs-lookup"><span data-stu-id="faaf4-106">master</span></span>


<span data-ttu-id="faaf4-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="faaf4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="faaf4-108">Indique le numéro qui identifie de manière unique un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="faaf4-108">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="faaf4-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="faaf4-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="faaf4-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="faaf4-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="faaf4-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="faaf4-111">Return value</span></span>
>>>>>>> <span data-ttu-id="faaf4-112">master</span><span class="sxs-lookup"><span data-stu-id="faaf4-112">master</span></span>

<span data-ttu-id="faaf4-113">Renvoie une valeur de type **Long** pouvant correspondre à l'une des constantes [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="faaf4-113">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="faaf4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="faaf4-114">Remarks</span></span>

<span data-ttu-id="faaf4-p101">Utilisez la propriété **Number** pour identifier l'erreur générée. La valeur de la propriété est un nombre unique qui correspond à la condition d'erreur.</span><span class="sxs-lookup"><span data-stu-id="faaf4-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="faaf4-117">La collection [Errors](errors-collection-ado.md) renvoie un HRESULT en format format hexadécimal (0x80004005 par exemple) ou une valeur longue (2147467259 par exemple).</span><span class="sxs-lookup"><span data-stu-id="faaf4-117">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="faaf4-118">Ces HRESULT peuvent être déclenchés par composants sous-jacents comme OLE DB ou même OLE.</span><span class="sxs-lookup"><span data-stu-id="faaf4-118">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="faaf4-119">Pour plus d’informations sur ces numéros, consultez le chapitre 16 de la *de référence du programmeur OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="faaf4-119">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

