---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtient une plage de temps prédéfinie pour une énumération de blocs de données de disponibilité pour un utilisateur.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430076"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="cd320-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="cd320-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="cd320-104">Obtient une plage de temps prédéfinie pour une énumération de blocs de données de disponibilité pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd320-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cd320-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="cd320-105">Quick info</span></span>

<span data-ttu-id="cd320-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="cd320-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="cd320-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd320-107">Parameters</span></span>

<span data-ttu-id="cd320-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="cd320-108">_prtmStart_</span></span>
  
> <span data-ttu-id="cd320-109">remarquer Une valeur de temps relative pour le début des informations de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="cd320-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="cd320-110">Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="cd320-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="cd320-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="cd320-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="cd320-112">remarquer Valeur d'heure relative pour la fin des informations de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="cd320-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="cd320-113">Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="cd320-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="cd320-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="cd320-114">Return values</span></span>

<span data-ttu-id="cd320-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="cd320-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd320-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd320-116">Remarks</span></span>

<span data-ttu-id="cd320-117">Un fournisseur de disponibilité appelle [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) pour définir la plage horaire pour une énumération.</span><span class="sxs-lookup"><span data-stu-id="cd320-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="cd320-118">Si [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) n'a pas été appelé, les valeurs par défaut pour **prtmStart** et **PrtmEnd** doivent être définies entre le 1er avril 1601 00:00:00Z et le 31 août 4500 11:59:59Z légumes.</span><span class="sxs-lookup"><span data-stu-id="cd320-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="cd320-119">En outre, vous ne devez pas définir l'heure de début sur une valeur supérieure à l'heure de fin.</span><span class="sxs-lookup"><span data-stu-id="cd320-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="cd320-120">**IFreeBusyData:: GetFBPublishRange** doit renvoyer les valeurs mises en cache pour la plage horaire définie par l'appel le plus récent pour **IFreeBusyData:: EnumBlocks** ou **IFreeBusyData:: SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="cd320-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd320-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd320-121">See also</span></span>

- [<span data-ttu-id="cd320-122">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="cd320-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="cd320-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="cd320-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="cd320-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="cd320-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

