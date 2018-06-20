---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Définit l’intervalle de temps pour une énumération des blocs de données de disponibilité d’un utilisateur.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782601"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="a5418-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="a5418-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="a5418-104">Définit l’intervalle de temps pour une énumération des blocs de données de disponibilité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5418-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a5418-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a5418-105">Quick info</span></span>

<span data-ttu-id="a5418-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="a5418-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="a5418-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5418-107">Parameters</span></span>

<span data-ttu-id="a5418-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="a5418-108">_rtmStart_</span></span>
  
> <span data-ttu-id="a5418-109">[in] Une valeur d’heure relative du début de la disponibilité des informations.</span><span class="sxs-lookup"><span data-stu-id="a5418-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="a5418-110">Cette valeur est le nombre de minutes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="a5418-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="a5418-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="a5418-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="a5418-112">[in] Une valeur d’heure relative à la fin des informations de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="a5418-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="a5418-113">Cette valeur est le nombre de minutes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="a5418-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a5418-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a5418-114">Return values</span></span>

<span data-ttu-id="a5418-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="a5418-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5418-116">Note</span><span class="sxs-lookup"><span data-stu-id="a5418-116">Remarks</span></span>

<span data-ttu-id="a5418-117">Cette méthode est utilisée pour indiquer la plage de temps des éléments de calendrier pour lequel récupérer les détails.</span><span class="sxs-lookup"><span data-stu-id="a5418-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="a5418-118">Les valeurs de *ftmStart* et *ftmEnd* sont mis en cache et retournés dans un autre appel de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="a5418-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5418-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5418-119">See also</span></span>

- [<span data-ttu-id="a5418-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="a5418-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="a5418-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="a5418-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="a5418-122">Utiliser l’heure relative pour accéder aux données et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="a5418-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

