---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Définit la plage de temps pour une éumération des blocs de données de la période de libre/occupé d’un utilisateur.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421661"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="60d7a-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="60d7a-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="60d7a-104">Définit la plage de temps pour une éumération des blocs de données de la période de libre/occupé d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60d7a-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="60d7a-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="60d7a-105">Quick info</span></span>

<span data-ttu-id="60d7a-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="60d7a-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="60d7a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60d7a-107">Parameters</span></span>

<span data-ttu-id="60d7a-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="60d7a-108">_rtmStart_</span></span>
  
> <span data-ttu-id="60d7a-109">[in] Valeur d’heure relative pour le début des informations de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="60d7a-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="60d7a-110">Cette valeur est le nombre de minutes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="60d7a-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="60d7a-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="60d7a-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="60d7a-112">[in] Valeur d’heure relative pour la fin des informations de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="60d7a-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="60d7a-113">Cette valeur est le nombre de minutes depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="60d7a-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="60d7a-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="60d7a-114">Return values</span></span>

<span data-ttu-id="60d7a-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="60d7a-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60d7a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="60d7a-116">Remarks</span></span>

<span data-ttu-id="60d7a-117">Cette méthode permet d’indiquer l’plage de temps des éléments de calendrier pour lesquels récupérer des détails.</span><span class="sxs-lookup"><span data-stu-id="60d7a-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="60d7a-118">Les valeurs  *de ftmStart*  et  *ftmEnd*  sont mises en cache et renvoyées dans un appel ultérieur de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="60d7a-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60d7a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60d7a-119">See also</span></span>

- [<span data-ttu-id="60d7a-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="60d7a-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="60d7a-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="60d7a-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="60d7a-122">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="60d7a-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

