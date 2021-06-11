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
# <a name="ienumfbblock"></a><span data-ttu-id="4877b-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="4877b-102">IEnumFBBlock</span></span>

<span data-ttu-id="4877b-103">Prend en charge l’accès et l’éumation des blocs de données de libre/occupé pour un utilisateur dans un délai.</span><span class="sxs-lookup"><span data-stu-id="4877b-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4877b-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4877b-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4877b-105">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="4877b-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="4877b-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4877b-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4877b-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="4877b-107">Provided by:</span></span>  <br/> |<span data-ttu-id="4877b-108">Fournisseur de services de libre-service</span><span class="sxs-lookup"><span data-stu-id="4877b-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="4877b-109">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="4877b-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4877b-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="4877b-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4877b-111">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="4877b-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4877b-112">Next</span><span class="sxs-lookup"><span data-stu-id="4877b-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="4877b-113">Obtient le nombre spécifié suivant de blocs de données de libre/occupé dans une éumération.</span><span class="sxs-lookup"><span data-stu-id="4877b-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="4877b-114">Skip</span><span class="sxs-lookup"><span data-stu-id="4877b-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="4877b-115">Ignore un nombre spécifié de blocs de données de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="4877b-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="4877b-116">Reset</span><span class="sxs-lookup"><span data-stu-id="4877b-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="4877b-117">Réinitialise l’éumérateur en redéfinissant le curseur au début.</span><span class="sxs-lookup"><span data-stu-id="4877b-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="4877b-118">Clone</span><span class="sxs-lookup"><span data-stu-id="4877b-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="4877b-119">Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en fixant le curseur au début de l’éumérateur.</span><span class="sxs-lookup"><span data-stu-id="4877b-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="4877b-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="4877b-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="4877b-121">Limite l’éumération à une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4877b-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4877b-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="4877b-122">Remarks</span></span>

<span data-ttu-id="4877b-123">Une éumération contient des blocs de données de libre/occupé qui ne se chevauchent pas dans le temps.</span><span class="sxs-lookup"><span data-stu-id="4877b-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="4877b-124">Lorsqu’un calendrier se chevauche, Outlook fusionne ces éléments pour former des blocs de libre/occupé non superposés dans l’éumération en fonction de cet ordre de priorité : absence du bureau, occupé, provisoire.</span><span class="sxs-lookup"><span data-stu-id="4877b-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="4877b-125">Un fournisseur de libre/occupé obtient cette interface et l’éumération pour un délai d’un utilisateur via [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="4877b-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4877b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4877b-126">See also</span></span>

- [<span data-ttu-id="4877b-127">À propos de l’API Disponibilité</span><span class="sxs-lookup"><span data-stu-id="4877b-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="4877b-128">Constantes (API de libre/occupé)</span><span class="sxs-lookup"><span data-stu-id="4877b-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="4877b-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="4877b-129">IFreeBusyData</span></span>](ifreebusydata.md)

