---
title: Gestion des erreurs dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d98b7cf1d6c5cdc8517ea2e653115d9a7c01e3c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593297"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="6951e-103">Gestion des erreurs dans MAPI</span><span class="sxs-lookup"><span data-stu-id="6951e-103">Error handling in MAPI</span></span>

<span data-ttu-id="6951e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6951e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6951e-105">Les valeurs de réussite, avertissement et d’erreur sont renvoyés en utilisant un nombre 32 bits connu ainsi poignée ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6951e-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="6951e-106">Une valeur HRESULT n’est vraiment pas un handle vers rien ; Il est simplement une valeur 32 bits avec plusieurs champs codé dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="6951e-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="6951e-107">Un résultat de zéro indique la réussite et un résultat différent de zéro indique l’échec.</span><span class="sxs-lookup"><span data-stu-id="6951e-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="6951e-108">MAPI sur les plateformes 32 bits fonctionne uniquement avec les valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6951e-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="6951e-109">L’illustration suivante montre le format HRESULT pour les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6951e-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="6951e-110">**Format HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6951e-110">**HRESULT format**</span></span>
  
<span data-ttu-id="6951e-111">![Format HRESULT] (media/amapi_49.gif "Format HRESULT")</span><span class="sxs-lookup"><span data-stu-id="6951e-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="6951e-112">Le bit poids fort HRESULT indique si la valeur renvoyée représente a réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="6951e-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="6951e-113">Si la valeur zéro, la valeur indique la réussite.</span><span class="sxs-lookup"><span data-stu-id="6951e-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="6951e-114">Si la valeur 1, elle indique échec.</span><span class="sxs-lookup"><span data-stu-id="6951e-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="6951e-115">R, C, N, les bits r sont réservés dans HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6951e-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="6951e-116">Le champ facility dans les deux versions indique le domaine de responsabilité de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="6951e-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="6951e-117">Il existe plusieurs fonctions, mais la plupart des erreurs MAPI utiliser FACILITY_ITF pour représenter les erreurs de l’interface.</span><span class="sxs-lookup"><span data-stu-id="6951e-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="6951e-118">Les fonctionnalités les plus courants qui sont actuellement utilisées sont : FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC et FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="6951e-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="6951e-119">Si les nouvelles installations sont nécessaires, Microsoft les alloue, car ils doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="6951e-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="6951e-120">Le tableau suivant décrit les divers champs des immobilisations.</span><span class="sxs-lookup"><span data-stu-id="6951e-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="6951e-121">Immobilisations</span><span class="sxs-lookup"><span data-stu-id="6951e-121">Facility</span></span>|<span data-ttu-id="6951e-122">Description</span><span class="sxs-lookup"><span data-stu-id="6951e-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="6951e-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="6951e-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="6951e-124">Pour les codes d’état courant applicables comme S_OK ou E_OUTOF_MEMORY ; la valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6951e-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="6951e-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="6951e-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="6951e-126">Pour la plupart des codes d’état renvoyés par les méthodes d’interface ; la valeur est définie par l’interface.</span><span class="sxs-lookup"><span data-stu-id="6951e-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="6951e-127">Autrement dit, deux valeurs HRESULT avec exactement la même valeur 32 bits renvoyé à partir de deux interfaces différentes peuvent avoir des significations différentes.</span><span class="sxs-lookup"><span data-stu-id="6951e-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="6951e-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="6951e-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="6951e-129">Erreurs d’interface de la liaison tardive [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6951e-129">For late binding [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="6951e-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="6951e-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="6951e-131">Pour les codes d’état renvoyés par les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="6951e-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="6951e-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="6951e-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="6951e-133">Pour les codes d’état renvoyés à partir d’appels de méthode [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) ou [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) relatifs au stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="6951e-133">For status codes returned from [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) or [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="6951e-134">Codes d’état avec des valeurs de code (16 bits inférieurs) dans les codes d’erreur de plage de Windows (c'est-à-dire, moins de 256) ont la même signification que les erreurs Windows correspondants.</span><span class="sxs-lookup"><span data-stu-id="6951e-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="6951e-135">Le champ code est un numéro unique assigné pour représenter l’erreur ou avertissement.</span><span class="sxs-lookup"><span data-stu-id="6951e-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

