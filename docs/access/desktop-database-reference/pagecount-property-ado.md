---
<span data-ttu-id="a5fc6-101"><<<<<<< Titre tête : TOCTitle PageCount propriété (ADO) : PageCount propriété (ADO) === titre : PageCount, propriété (ADO) TOCTitle : PageCount, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5fc6-101"><<<<<<< HEAD title: PageCount Property (ADO) TOCTitle: PageCount Property (ADO) ======= title: PageCount property (ADO) TOCTitle: PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a5fc6-102">Master ms:assetid : 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID : ms.date 48546609 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="a5fc6-102">master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a5fc6-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="a5fc6-103"><<<<<<< HEAD</span></span>
# <a name="pagecount-property-ado"></a><span data-ttu-id="a5fc6-104">PageCount, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5fc6-104">PageCount Property (ADO)</span></span>
=======
# <a name="pagecount-property-ado"></a><span data-ttu-id="a5fc6-105">PageCount, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5fc6-105">PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a5fc6-106">master</span><span class="sxs-lookup"><span data-stu-id="a5fc6-106">master</span></span>


<span data-ttu-id="a5fc6-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5fc6-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5fc6-108">Indique le nombre de pages de données que contient l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5fc6-108">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

<span data-ttu-id="a5fc6-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="a5fc6-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a5fc6-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5fc6-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a5fc6-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5fc6-111">Return value</span></span>
>>>>>>> <span data-ttu-id="a5fc6-112">master</span><span class="sxs-lookup"><span data-stu-id="a5fc6-112">master</span></span>

<span data-ttu-id="a5fc6-113">Retourne une valeur de type **Long** qui indique le nombre de pages dans le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a5fc6-113">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5fc6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5fc6-114">Remarks</span></span>

<span data-ttu-id="a5fc6-115">Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a5fc6-115">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="a5fc6-116">*Les pages* sont des groupes d’enregistrements dont la taille est égale à [la propriété PageSize](pagesize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a5fc6-116">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="a5fc6-117">Même si la dernière page est incomplète et que le nombre d'enregistrements qu'elle contient est inférieur à la valeur de **PageSize**, elle est considérée comme une page supplémentaire dans la valeur **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="a5fc6-117">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="a5fc6-118">Si l'objet **Recordset** ne prend pas en charge cette propriété, la valeur sera -1, pour indiquer que la propriété **PageCount** ne peut pas être déterminée.</span><span class="sxs-lookup"><span data-stu-id="a5fc6-118">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="a5fc6-119">Pour plus d'informations sur les fonctionnalités relatives aux pages, voir les propriétés **PageSize** et [AbsolutePage](absolutepage-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5fc6-119">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

