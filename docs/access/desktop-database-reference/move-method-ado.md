---
title: Move, méthode - ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55439f14cd2a498ec2592c533dd308f82798b1e8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929446"
---
# <a name="move-method-ado"></a><span data-ttu-id="a01ff-102">Move, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a01ff-102">Move method (ADO)</span></span>


<span data-ttu-id="a01ff-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a01ff-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a01ff-104">Déplace la position de l'enregistrement actif dans un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a01ff-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a01ff-105">Syntax</span></span>

<span data-ttu-id="a01ff-106">*jeu d’enregistrements*. Déplacer *NbEnregistrements*, *Démarrer*</span><span class="sxs-lookup"><span data-stu-id="a01ff-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="a01ff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a01ff-107">Parameters</span></span>

  - <span data-ttu-id="a01ff-108">*NbEnregistrements*</span><span class="sxs-lookup"><span data-stu-id="a01ff-108">*NumRecords*</span></span>

  - <span data-ttu-id="a01ff-109">Expression de type **Long** signée qui spécifie le nombre d'enregistrements dont la position de l'enregistrement actif sera déplacée.</span><span class="sxs-lookup"><span data-stu-id="a01ff-109">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>

  - <span data-ttu-id="a01ff-110">*Début*</span><span class="sxs-lookup"><span data-stu-id="a01ff-110">*Start*</span></span>

  - <span data-ttu-id="a01ff-p101">Facultatif. Valeur de type **String** ou **Variant** qui correspond à un signet. Vous pouvez également utiliser une valeur [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="a01ff-p101">Optional. A **String** value or **Variant** that evaluates to a bookmark. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01ff-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a01ff-114">Remarks</span></span>

<span data-ttu-id="a01ff-115">La méthode **Move** est prise en charge sur tous les objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a01ff-115">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="a01ff-p102">Si l'argument *NumRecords* est supérieur à zéro, la position de l'enregistrement actif est avancée (vers la fin du **jeu d'enregistrements**). Si l'argument *NumRecords* est inférieur à zéro, la position de l'enregistrement actif est déplacée vers l'arrière (vers le début du **jeu d'enregistrements**).</span><span class="sxs-lookup"><span data-stu-id="a01ff-p102">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="a01ff-118">Si l’appel de **déplacer** la méthode déplace la position d’enregistrement actuelle vers un point situé avant le premier enregistrement, ADO définit l’enregistrement actif à la position avant le premier enregistrement du jeu d’enregistrements (la[propriété BOF](bof-eof-properties-ado.md) a **la valeur True**).</span><span class="sxs-lookup"><span data-stu-id="a01ff-118">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="a01ff-119">Une tentative de déplacement arrière lorsque la propriété **BOF** a déjà la valeur **True** génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="a01ff-119">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a01ff-120">Si l’appel de **déplacer** la méthode déplace la position d’enregistrement actuelle vers un point d’après le dernier enregistrement, ADO définit l’enregistrement actif à la position après le dernier enregistrement du jeu d’enregistrements (la[propriété EOF](bof-eof-properties-ado.md) a **la valeur True**).</span><span class="sxs-lookup"><span data-stu-id="a01ff-120">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="a01ff-121">Une tentative de déplacement vers l'avant lorsque la propriété **EOF** a déjà la valeur **True** génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="a01ff-121">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a01ff-122">L'appel de la méthode **Move** à partir d'un objet **Recordset** vide génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="a01ff-122">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="a01ff-123">Si vous passez l’argument *début* , le déplacement est par rapport à l’objet record à ce signet, en supposant que l’objet **Recordset** prend en charge les signets.</span><span class="sxs-lookup"><span data-stu-id="a01ff-123">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="a01ff-124">S'il n'est pas spécifié, le déplacement est effectué par rapport à l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="a01ff-124">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="a01ff-125">Si vous utilisez la propriété [CacheSize](cachesize-property-ado.md) pour cache localement des enregistrements à partir du fournisseur, en passant un argument *NbEnregistrements* qui déplace la position d’enregistrement actif en dehors du groupe actuel d’enregistrements mis en cache force ADO à récupérer un nouveau groupe d’enregistrements, à partir de l’enregistrement de destination.</span><span class="sxs-lookup"><span data-stu-id="a01ff-125">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="a01ff-126">La propriété **CacheSize** détermine la taille du nouveau groupe extrait et l’enregistrement de destination est le premier enregistrement récupéré.</span><span class="sxs-lookup"><span data-stu-id="a01ff-126">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="a01ff-127">Si l’objet **Recordset** est avant uniquement, un utilisateur peut néanmoins passer un argument *NbEnregistrements* inférieur à zéro, à condition que la destination soit dans l’ensemble actuel d’enregistrements mis en cache.</span><span class="sxs-lookup"><span data-stu-id="a01ff-127">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="a01ff-128">Si l'appel de la méthode **Move** déplace la position d'enregistrement actif vers un enregistrement placé avant le premier enregistrement mis en cache, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="a01ff-128">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="a01ff-129">Par conséquent, vous pouvez utiliser un cache d'enregistrements qui prend en charge le défilement bi-directionnel sur un fournisseur qui ne prend en charge que le défilement avant.</span><span class="sxs-lookup"><span data-stu-id="a01ff-129">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="a01ff-130">Dans la mesure où les enregistrements mis en cache sont chargés en mémoire, évitez de mettre en cache plus d'enregistrements qu'il n'est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a01ff-130">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="a01ff-131">Même si un objet **Recordset** avant seulement peut prendre en charge ce type de déplacement arrière, l'appel de la méthode [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) sur un objet **Recordset** avant seulement génère néanmoins une erreur.</span><span class="sxs-lookup"><span data-stu-id="a01ff-131">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="a01ff-p108">[!REMARQUE] La prise en charge d'un déplacement arrière dans un objet **Recordset** avant seulement dépend de votre fournisseur et reste donc imprévisible. Si l'enregistrement actif a été placé après le dernier enregistrement de l'objet **Recordset**, un **déplacement** arrière est susceptible d'entraîner une position active incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a01ff-p108">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider. If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>


