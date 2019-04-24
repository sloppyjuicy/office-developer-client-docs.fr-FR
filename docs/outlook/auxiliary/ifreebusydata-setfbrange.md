---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Définit la plage de temps pour une énumération de blocs de données de disponibilité pour un utilisateur.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317478"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="29bf6-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="29bf6-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="29bf6-104">Définit la plage de temps pour une énumération de blocs de données de disponibilité pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29bf6-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="29bf6-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="29bf6-105">Quick info</span></span>

<span data-ttu-id="29bf6-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="29bf6-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="29bf6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29bf6-107">Parameters</span></span>

<span data-ttu-id="29bf6-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="29bf6-108">_rtmStart_</span></span>
  
> <span data-ttu-id="29bf6-109">dans Une valeur de temps relative pour le début des informations de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="29bf6-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="29bf6-110">Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="29bf6-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="29bf6-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="29bf6-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="29bf6-112">dans Valeur d'heure relative pour la fin des informations de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="29bf6-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="29bf6-113">Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="29bf6-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="29bf6-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="29bf6-114">Return values</span></span>

<span data-ttu-id="29bf6-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="29bf6-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29bf6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="29bf6-116">Remarks</span></span>

<span data-ttu-id="29bf6-117">Cette méthode est utilisée pour indiquer la plage horaire des éléments de calendrier pour lesquels récupérer les détails.</span><span class="sxs-lookup"><span data-stu-id="29bf6-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="29bf6-118">Les valeurs de *ftmStart* et *ftmEnd* sont mises en cache et renvoyées lors d'un appel ultérieur de [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="29bf6-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29bf6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29bf6-119">See also</span></span>

- [<span data-ttu-id="29bf6-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="29bf6-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="29bf6-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="29bf6-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="29bf6-122">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="29bf6-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

