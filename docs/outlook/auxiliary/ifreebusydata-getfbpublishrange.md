---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtient une énumération des informations de disponibilité des blocs de données pour un utilisateur une plage de temps prédéfini.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782583"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="1f0a5-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="1f0a5-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="1f0a5-104">Obtient une énumération des informations de disponibilité des blocs de données pour un utilisateur une plage de temps prédéfini.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1f0a5-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1f0a5-105">Quick info</span></span>

<span data-ttu-id="1f0a5-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="1f0a5-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="1f0a5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f0a5-107">Parameters</span></span>

<span data-ttu-id="1f0a5-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="1f0a5-108">_prtmStart_</span></span>
  
> <span data-ttu-id="1f0a5-109">[out] Une valeur d’heure relative du début de la disponibilité des informations.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="1f0a5-110">Cette valeur est le nombre de minutes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="1f0a5-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="1f0a5-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="1f0a5-112">[out] Une valeur d’heure relative à la fin des informations de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="1f0a5-113">Cette valeur est le nombre de minutes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1f0a5-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1f0a5-114">Return values</span></span>

<span data-ttu-id="1f0a5-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f0a5-116">Note</span><span class="sxs-lookup"><span data-stu-id="1f0a5-116">Remarks</span></span>

<span data-ttu-id="1f0a5-117">Un fournisseur et de disponibilité appelle [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) pour définir la période pour une énumération.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="1f0a5-118">Si [l’IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) n’a pas été appelée, les valeurs par défaut pour **prtmStart** et **prtmEnd** doivent être définies entre le 1er avril 1601 00:00:00Z et le 31 août 4500 11:59:59Z respectivement.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="1f0a5-119">En outre, vous ne devez pas définir l’heure de début est supérieure à l’heure de fin.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="1f0a5-120">**IFreeBusyData::GetFBPublishRange** doit renvoyer que les valeurs mises en cache pour la période définie par l’appel le plus récent pour **IFreeBusyData::EnumBlocks** ou **IFreeBusyData::SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="1f0a5-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f0a5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f0a5-121">See also</span></span>

- [<span data-ttu-id="1f0a5-122">Utiliser l’heure relative pour accéder aux données et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="1f0a5-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="1f0a5-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="1f0a5-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="1f0a5-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="1f0a5-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

