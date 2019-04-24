---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317625"
---
# <a name="ienumfbblock"></a><span data-ttu-id="d8db4-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="d8db4-102">IEnumFBBlock</span></span>

<span data-ttu-id="d8db4-103">Prend en charge l'accès et l'énumération des blocs de données de disponibilité d'un utilisateur dans un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="d8db4-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d8db4-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d8db4-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8db4-105">Hérite de:</span><span class="sxs-lookup"><span data-stu-id="d8db4-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="d8db4-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8db4-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d8db4-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="d8db4-107">Provided by:</span></span>  <br/> |<span data-ttu-id="d8db4-108">Fournisseur de disponibilité</span><span class="sxs-lookup"><span data-stu-id="d8db4-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="d8db4-109">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="d8db4-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d8db4-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="d8db4-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d8db4-111">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="d8db4-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d8db4-112">Next</span><span class="sxs-lookup"><span data-stu-id="d8db4-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="d8db4-113">Obtient le prochain nombre spécifié de blocs de données de disponibilité dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="d8db4-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="d8db4-114">Skip</span><span class="sxs-lookup"><span data-stu-id="d8db4-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="d8db4-115">Ignore un nombre spécifié de blocs de données de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d8db4-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="d8db4-116">Reset</span><span class="sxs-lookup"><span data-stu-id="d8db4-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="d8db4-117">Réinitialise l'énumérateur en définissant le curseur au début.</span><span class="sxs-lookup"><span data-stu-id="d8db4-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="d8db4-118">Clone</span><span class="sxs-lookup"><span data-stu-id="d8db4-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="d8db4-119">Crée une copie de l'énumérateur à l'aide de la même restriction temporelle, mais en définissant le curseur au début de l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="d8db4-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d8db4-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="d8db4-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="d8db4-121">Limite l'énumération à une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8db4-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8db4-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8db4-122">Remarks</span></span>

<span data-ttu-id="d8db4-123">Une énumération contient des blocs de données de disponibilité qui ne se chevauchent pas dans le temps.</span><span class="sxs-lookup"><span data-stu-id="d8db4-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="d8db4-124">Lorsqu'il y a des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour créer des blocs de disponibilité qui ne se chevauchent pas dans l'énumération en fonction de cet ordre de priorité: absent (e) du bureau, occupé (e).</span><span class="sxs-lookup"><span data-stu-id="d8db4-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="d8db4-125">Un fournisseur de disponibilité obtient cette interface et l'énumération pour un intervalle de temps pour un utilisateur via [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="d8db4-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8db4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8db4-126">See also</span></span>

- [<span data-ttu-id="d8db4-127">À propos de l'API de type disponible/occupé</span><span class="sxs-lookup"><span data-stu-id="d8db4-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="d8db4-128">Constantes (API de disponibilité)</span><span class="sxs-lookup"><span data-stu-id="d8db4-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="d8db4-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="d8db4-129">IFreeBusyData</span></span>](ifreebusydata.md)

