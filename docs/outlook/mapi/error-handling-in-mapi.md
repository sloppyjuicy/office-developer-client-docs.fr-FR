---
title: Gestion des erreurs dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287278"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="dc899-103">Gestion des erreurs dans MAPI</span><span class="sxs-lookup"><span data-stu-id="dc899-103">Error handling in MAPI</span></span>

<span data-ttu-id="dc899-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc899-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc899-105">Les valeurs de réussite, d’avertissement et d’erreur sont renvoyées à l’aide d’un nombre 32 bits appelé handle de résultats, ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="dc899-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="dc899-106">Un HRESULT n’est vraiment pas un handle vers quoi que ce soit ; Il s’agit simplement d’une valeur 32 bits avec plusieurs champs codés dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="dc899-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="dc899-107">Un résultat zéro indique un succès et un résultat non nul indique un échec.</span><span class="sxs-lookup"><span data-stu-id="dc899-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="dc899-108">MAPI sur les plateformes 32 bits fonctionne uniquement avec les valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="dc899-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="dc899-109">L’illustration suivante montre le format HRESULT pour les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dc899-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="dc899-110">**Format HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc899-110">**HRESULT format**</span></span>
  
<span data-ttu-id="dc899-111">![Format HRESULT au](media/amapi_49.gif "format HRESULT")</span><span class="sxs-lookup"><span data-stu-id="dc899-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="dc899-112">Le bit d’ordre élevé dans hrESULT indique si la valeur de retour représente la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="dc899-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="dc899-113">Si la valeur est définie sur zéro, la valeur indique la réussite.</span><span class="sxs-lookup"><span data-stu-id="dc899-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="dc899-114">Si elle est définie sur 1, elle indique un échec.</span><span class="sxs-lookup"><span data-stu-id="dc899-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="dc899-115">Les bits R, C, N et r sont réservés dans hrESULT.</span><span class="sxs-lookup"><span data-stu-id="dc899-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="dc899-116">Le champ de la facilité dans les deux versions indique la zone de responsabilité de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dc899-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="dc899-117">Il existe plusieurs installations, mais la grande majorité des erreurs MAPI utilisent FACILITY_ITF pour représenter des erreurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="dc899-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="dc899-118">Les installations les plus courantes actuellement utilisées sont les FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC et FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="dc899-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="dc899-119">Si de nouvelles installations sont nécessaires, Microsoft les alloue, car elles doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="dc899-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="dc899-120">Le tableau suivant décrit les différents champs d’installation.</span><span class="sxs-lookup"><span data-stu-id="dc899-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="dc899-121">Facility</span><span class="sxs-lookup"><span data-stu-id="dc899-121">Facility</span></span>|<span data-ttu-id="dc899-122">Description</span><span class="sxs-lookup"><span data-stu-id="dc899-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc899-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="dc899-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="dc899-124">Pour les codes d’état courants applicables à grande S_OK ou E_OUTOF_MEMORY ; la valeur est zéro.</span><span class="sxs-lookup"><span data-stu-id="dc899-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="dc899-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="dc899-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="dc899-126">Pour la plupart des codes d’état renvoyés à partir des méthodes d’interface ; la valeur est définie par l’interface.</span><span class="sxs-lookup"><span data-stu-id="dc899-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="dc899-127">Autrement dit, deux valeurs HRESULT avec exactement la même valeur 32 bits renvoyées à partir de deux interfaces différentes peuvent avoir des significations différentes.</span><span class="sxs-lookup"><span data-stu-id="dc899-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="dc899-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="dc899-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="dc899-129">Pour les erreurs d’interface [IDispatch de](https://msdn.microsoft.com/library/ms221608.aspx) liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="dc899-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="dc899-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="dc899-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="dc899-131">Pour les codes d’état renvoyés par les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="dc899-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="dc899-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="dc899-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="dc899-133">Pour les codes d’état renvoyés par les appels de méthode [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relatifs au stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="dc899-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="dc899-134">Les codes d’état avec des valeurs de code (moins de 16 bits) dans la plage de codes d’erreur Windows (c’est-à-dire, inférieur à 256) ont la même signification que les erreurs Windows correspondantes.</span><span class="sxs-lookup"><span data-stu-id="dc899-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="dc899-135">Le champ de code est un numéro unique affecté pour représenter l’erreur ou l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="dc899-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

