---
<span data-ttu-id="5dd0d-101"><<<<<<< Titre tête : TOCTitle PageSize propriété (ADO) : PageSize propriété (ADO) === titre : PageSize, propriété (ADO) TOCTitle : PageSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5dd0d-101"><<<<<<< HEAD title: PageSize Property (ADO) TOCTitle: PageSize Property (ADO) ======= title: PageSize property (ADO) TOCTitle: PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5dd0d-102">Master ms:assetid : da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl : https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID : ms.date 48548079 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="5dd0d-102">master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5dd0d-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5dd0d-103"><<<<<<< HEAD</span></span>
# <a name="pagesize-property-ado"></a><span data-ttu-id="5dd0d-104">PageSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5dd0d-104">PageSize Property (ADO)</span></span>
=======
# <a name="pagesize-property-ado"></a><span data-ttu-id="5dd0d-105">PageSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5dd0d-105">PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5dd0d-106">master</span><span class="sxs-lookup"><span data-stu-id="5dd0d-106">master</span></span>


<span data-ttu-id="5dd0d-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dd0d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5dd0d-108">Indique combien d'enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5dd0d-108">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="5dd0d-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5dd0d-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="5dd0d-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5dd0d-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="5dd0d-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5dd0d-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="5dd0d-112">master</span><span class="sxs-lookup"><span data-stu-id="5dd0d-112">master</span></span>

<span data-ttu-id="5dd0d-p101">Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd0d-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dd0d-115">Remarks</span></span>

<span data-ttu-id="5dd0d-116"><<<<<<< Tête d’utiliser la propriété **PageSize** pour déterminer le nombre d’enregistrements constituent une page logique de données.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-116"><<<<<<< HEAD Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="5dd0d-117">La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-117">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="5dd0d-118">Ceci s'avère utile dans les scénarios de serveurs Web, pour offrir aux utilisateurs la possibilité de passer d'une page de données à une autre et de consulter un certain nombre d'enregistrements à la fois.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-118">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
<span data-ttu-id="5dd0d-119">=== Utilisez la propriété **PageSize** pour déterminer le nombre d’enregistrements constituent une page logique de données.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-119">======= Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="5dd0d-120">La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-120">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="5dd0d-121">Cela est utile dans les scénarios de serveur web lorsque vous souhaitez permettre à l’utilisateur de parcourir les données, consulter un certain nombre d’enregistrements à la fois.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-121">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
>>>>>>> <span data-ttu-id="5dd0d-122">master</span><span class="sxs-lookup"><span data-stu-id="5dd0d-122">master</span></span>

<span data-ttu-id="5dd0d-123">Cette propriété peut être définie à tout moment ; sa valeur est utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="5dd0d-123">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

