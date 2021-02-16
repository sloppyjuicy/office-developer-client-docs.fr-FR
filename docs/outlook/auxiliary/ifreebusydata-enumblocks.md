---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtient une interface qui éumène les blocs de données de libre/occupé pour un utilisateur dans un délai spécifié.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317555"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="a23b2-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="a23b2-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="a23b2-104">Obtient une interface qui éumène les blocs de données de libre/occupé pour un utilisateur dans un délai spécifié.</span><span class="sxs-lookup"><span data-stu-id="a23b2-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a23b2-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a23b2-105">Quick info</span></span>

<span data-ttu-id="a23b2-106">Voir [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="a23b2-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="a23b2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a23b2-107">Parameters</span></span>

<span data-ttu-id="a23b2-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="a23b2-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="a23b2-109">[out] Interface qui permet d’éumer les blocs de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="a23b2-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="a23b2-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="a23b2-110">_ftmStart_</span></span>
  
> <span data-ttu-id="a23b2-111">[in] Heure de début de l’éumération.</span><span class="sxs-lookup"><span data-stu-id="a23b2-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="a23b2-112">Il est exprimé en [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="a23b2-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="a23b2-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="a23b2-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="a23b2-114">[in] Heure de fin de l’éumération.</span><span class="sxs-lookup"><span data-stu-id="a23b2-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="a23b2-115">Il est exprimé en **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="a23b2-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a23b2-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a23b2-116">Return values</span></span>

<span data-ttu-id="a23b2-117">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="a23b2-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a23b2-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="a23b2-118">Remarks</span></span>

<span data-ttu-id="a23b2-119">Cette méthode permet d’indiquer l’plage de temps des éléments de calendrier pour lesquels récupérer des détails.</span><span class="sxs-lookup"><span data-stu-id="a23b2-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="a23b2-120">Les valeurs  *de ftmStart* et *ftmEnd* sont mises en cache et renvoyées dans un appel ultérieur de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="a23b2-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="a23b2-121">Un fournisseur de libre/occupé peut également utiliser par la suite l’interface [IEnumFBBlock](ienumfbblock.md) renvoyée pour accéder à l’éumération.</span><span class="sxs-lookup"><span data-stu-id="a23b2-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a23b2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a23b2-122">See also</span></span>

- [<span data-ttu-id="a23b2-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="a23b2-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="a23b2-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="a23b2-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="a23b2-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="a23b2-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="a23b2-126">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="a23b2-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

