---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782593"
---
# <a name="ienumfbblock"></a><span data-ttu-id="ca896-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="ca896-102">IEnumFBBlock</span></span>

<span data-ttu-id="ca896-103">Prend en charge l’accès et l’énumération des informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps.</span><span class="sxs-lookup"><span data-stu-id="ca896-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ca896-104">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ca896-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca896-105">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="ca896-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="ca896-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca896-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ca896-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="ca896-107">Provided by:</span></span>  <br/> |<span data-ttu-id="ca896-108">Fournisseur de disponibilité</span><span class="sxs-lookup"><span data-stu-id="ca896-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="ca896-109">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="ca896-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ca896-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="ca896-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ca896-111">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="ca896-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ca896-112">Suivant</span><span class="sxs-lookup"><span data-stu-id="ca896-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="ca896-113">Obtient le nombre spécifié suivant de blocs de données et de disponibilité dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="ca896-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="ca896-114">Ignorer</span><span class="sxs-lookup"><span data-stu-id="ca896-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="ca896-115">Ignore un nombre spécifié de blocs de données et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="ca896-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="ca896-116">Reset</span><span class="sxs-lookup"><span data-stu-id="ca896-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="ca896-117">Réinitialise l’énumérateur en définissant le curseur au début.</span><span class="sxs-lookup"><span data-stu-id="ca896-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="ca896-118">Clone</span><span class="sxs-lookup"><span data-stu-id="ca896-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="ca896-119">Crée une copie de l’énumérateur, à l’aide de la même restriction mais définissant le curseur au début de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="ca896-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="ca896-120">Restreindre</span><span class="sxs-lookup"><span data-stu-id="ca896-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="ca896-121">Limite de l’énumération à une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ca896-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca896-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca896-122">Remarks</span></span>

<span data-ttu-id="ca896-123">Une énumération contient des informations de disponibilité des blocs de données qui ne se chevauchent pas dans le temps.</span><span class="sxs-lookup"><span data-stu-id="ca896-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="ca896-124">Lorsqu’il existe des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour former des blocs de disponibilité sans chevauchement de l’énumération basée sur cet ordre de priorité : hors du bureau, provisoire, occupé (e).</span><span class="sxs-lookup"><span data-stu-id="ca896-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="ca896-125">Un fournisseur et de disponibilité permet d’obtenir cette interface et l’énumération pour une plage de temps pour un utilisateur par le biais de [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="ca896-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca896-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca896-126">See also</span></span>

- [<span data-ttu-id="ca896-127">À propos de l'API de type disponible/occupé</span><span class="sxs-lookup"><span data-stu-id="ca896-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="ca896-128">Constantes (disponibilité API)</span><span class="sxs-lookup"><span data-stu-id="ca896-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="ca896-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="ca896-129">IFreeBusyData</span></span>](ifreebusydata.md)

