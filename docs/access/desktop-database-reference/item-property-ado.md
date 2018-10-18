---
<span data-ttu-id="71632-101"><<<<<<< Titre tête : élément propriété (ADO) TOCTitle : élément de propriété (ADO) === titre : Item, propriété (ADO) TOCTitle : Item, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="71632-101"><<<<<<< HEAD title: Item Property (ADO) TOCTitle: Item Property (ADO) ======= title: Item property (ADO) TOCTitle: Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="71632-102">Master ms:assetid : 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID : ms.date 48545767 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="71632-102">master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="71632-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="71632-103"><<<<<<< HEAD</span></span>
# <a name="item-property-ado"></a><span data-ttu-id="71632-104">Item, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="71632-104">Item Property (ADO)</span></span>
=======
# <a name="item-property-ado"></a><span data-ttu-id="71632-105">Item, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="71632-105">Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="71632-106">master</span><span class="sxs-lookup"><span data-stu-id="71632-106">master</span></span>

<span data-ttu-id="71632-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="71632-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="71632-108">Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.</span><span class="sxs-lookup"><span data-stu-id="71632-108">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="71632-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71632-109">Syntax</span></span>

<span data-ttu-id="71632-110">Définir*l’objet* = *collection*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="71632-110">Set*object* = *collection*.Item ( Index )</span></span>

<span data-ttu-id="71632-111"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="71632-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="71632-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71632-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="71632-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71632-113">Return value</span></span>
>>>>>>> <span data-ttu-id="71632-114">master</span><span class="sxs-lookup"><span data-stu-id="71632-114">master</span></span>

<span data-ttu-id="71632-115">Renvoie une référence à un objet.</span><span class="sxs-lookup"><span data-stu-id="71632-115">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="71632-116">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71632-116">Parameters</span></span>

- <span data-ttu-id="71632-117">*Index*</span><span class="sxs-lookup"><span data-stu-id="71632-117">*Index*</span></span>

- <span data-ttu-id="71632-118">Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.</span><span class="sxs-lookup"><span data-stu-id="71632-118">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="71632-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="71632-119">Remarks</span></span>

<span data-ttu-id="71632-120">Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection.</span><span class="sxs-lookup"><span data-stu-id="71632-120">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="71632-121">Si **l’élément** ne peut pas trouver un objet dans la collection correspondant à l’argument *Index* , une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="71632-121">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="71632-122">Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.</span><span class="sxs-lookup"><span data-stu-id="71632-122">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="71632-123">La propriété **Item** est la propriété par défaut de toutes les collections ; les formes de syntaxe suivantes sont donc interchangeables :</span><span class="sxs-lookup"><span data-stu-id="71632-123">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
