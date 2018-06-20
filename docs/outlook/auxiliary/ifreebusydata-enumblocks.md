---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtient une interface qui énumère les informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps spécifié.
ms.openlocfilehash: ab377b1029296b6b4bac68d7169dcf7b8dcd8b87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782588"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="a6a12-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="a6a12-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="a6a12-104">Obtient une interface qui énumère les informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="a6a12-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a6a12-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a6a12-105">Quick info</span></span>

<span data-ttu-id="a6a12-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="a6a12-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="a6a12-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6a12-107">Parameters</span></span>

<span data-ttu-id="a6a12-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="a6a12-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="a6a12-109">[out] Une interface pour énumérer les blocs de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="a6a12-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="a6a12-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="a6a12-110">_ftmStart_</span></span>
  
> <span data-ttu-id="a6a12-111">[in] Heure de début de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="a6a12-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="a6a12-112">Il est exprimé en [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6a12-112">It is expressed in [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="a6a12-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="a6a12-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="a6a12-114">[in] Heure de fin de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="a6a12-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="a6a12-115">Il est exprimé en **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="a6a12-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a6a12-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a6a12-116">Return values</span></span>

<span data-ttu-id="a6a12-117">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="a6a12-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6a12-118">Note</span><span class="sxs-lookup"><span data-stu-id="a6a12-118">Remarks</span></span>

<span data-ttu-id="a6a12-119">Cette méthode est utilisée pour indiquer la plage de temps des éléments de calendrier pour lequel récupérer les détails.</span><span class="sxs-lookup"><span data-stu-id="a6a12-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="a6a12-120">Les valeurs de *ftmStart* et *ftmEnd* sont mis en cache et retournés dans un autre appel de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="a6a12-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="a6a12-121">Un fournisseur et de disponibilité peut également ensuite utiliser l’interface [IEnumFBBlock](ienumfbblock.md) retournée pour accéder l’énumération.</span><span class="sxs-lookup"><span data-stu-id="a6a12-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6a12-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6a12-122">See also</span></span>

- [<span data-ttu-id="a6a12-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="a6a12-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="a6a12-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="a6a12-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="a6a12-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="a6a12-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="a6a12-126">Utiliser l’heure relative pour accéder aux données et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="a6a12-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

