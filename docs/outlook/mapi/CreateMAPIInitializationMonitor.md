---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Moniteur d’initialisation MAPI
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062052"
---
# <a name="createmapiinitializationmonitor"></a><span data-ttu-id="a3e5b-103">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="a3e5b-103">CreateMAPIInitializationMonitor</span></span>

<span data-ttu-id="a3e5b-104">**S’applique** à : Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="a3e5b-104">**Applies to**: Outlook 2016 | Outlook 2019</span></span>
  
## <a name="mapi-initialization-monitor"></a><span data-ttu-id="a3e5b-105">Moniteur d’initialisation MAPI</span><span class="sxs-lookup"><span data-stu-id="a3e5b-105">MAPI Initialization Monitor</span></span>

<span data-ttu-id="a3e5b-106">Parfois, une application qui utilise MAPI peut vouloir savoir quand l’initialisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-106">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="a3e5b-107">Par exemple, il a plusieurs threads qui pourraient initialiser MAPI, ou en réponse à l’initialisation de MAPI l’application souhaiterait effectuer un travail, mais ne souhaite pas toujours faire tourner la pile MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-107">For example, it have multiple threads which could initialize MAPI, or in response to MAPI being initialize the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="a3e5b-108">Le moniteur d’initialisation fournit cette fonctionnalité via une fonction (exportée à partir de OLMAPI32.DLL) et quelques interfaces simples décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-108">The initialization monitor provides this functionality through a function (exported from OLMAPI32.DLL) and a couple of simple interfaces described below.</span></span>

<span data-ttu-id="a3e5b-109">Il s’agit du point d’entrée exporté à partir de OLMAPI32.DLL cela permet à l’appelant de récupérer une interface pour interroger l’état d’initialisation actuel, configurer un rappel pour l’achèvement de l’initialisation ou bloquer le thread actuel jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-109">This is entry point exported from OLMAPI32.DLL this allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="a3e5b-110">L’objet renvoyé à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n’importe quel thread, pas seulement du thread qui l’a récupéré.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-110">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="a3e5b-111">En outre, contrairement aux autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être ré-utilisé entre les sessions d’initialisation et peut être utilisé avant ou après l’appel de MAPIInitialize.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-111">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="a3e5b-112">Renvoie le succès ou l’échec via un HRESULT standard COM et affecte un paramètre de sortie à une instance de IMAPIInitMonitor.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-112">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a><span data-ttu-id="a3e5b-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span><span class="sxs-lookup"><span data-stu-id="a3e5b-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span></span>

<span data-ttu-id="a3e5b-114">Ce point d’entrée exporté à partir de OLMAPI32.DLL permet à l’appelant de récupérer une interface pour interroger l’état d’initialisation actuel, configurer un rappel pour l’achèvement de l’initialisation ou bloquer le thread actuel jusqu’à ce qu’il soit terminé.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-114">This entry point exported from OLMAPI32.DLL allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="a3e5b-115">L’objet renvoyé à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n’importe quel thread, pas seulement du thread qui l’a récupéré.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-115">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="a3e5b-116">En outre, contrairement aux autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être ré-utilisé entre les sessions d’initialisation et peut être utilisé avant ou après l’appel de MAPIInitialize.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-116">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="a3e5b-117">Renvoie le succès ou l’échec via un HRESULT standard COM et affecte un paramètre de sortie à une instance de IMAPIInitMonitor.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-117">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a3e5b-118">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a3e5b-118">Quick info</span></span>

| <span data-ttu-id="a3e5b-119">identifiant</span><span class="sxs-lookup"><span data-stu-id="a3e5b-119">identifier</span></span> | <span data-ttu-id="a3e5b-120">result</span><span class="sxs-lookup"><span data-stu-id="a3e5b-120">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="a3e5b-121">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="a3e5b-121">Exported by:</span></span>  <br/> |<span data-ttu-id="a3e5b-122">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a3e5b-122">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a3e5b-123">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a3e5b-123">Called by:</span></span>  <br/> |<span data-ttu-id="a3e5b-124">Client</span><span class="sxs-lookup"><span data-stu-id="a3e5b-124">Client</span></span>  <br/> |
|<span data-ttu-id="a3e5b-125">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a3e5b-125">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3e5b-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="a3e5b-126">Outlook</span></span>  <br/> |

## <a name="parameters"></a><span data-ttu-id="a3e5b-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="a3e5b-127">Parameters</span></span>
  
 <span data-ttu-id="a3e5b-128">_ppInitMonitor_</span><span class="sxs-lookup"><span data-stu-id="a3e5b-128">_ppInitMonitor_</span></span>
> <span data-ttu-id="a3e5b-129">[out] Pointeur pour recevoir l’instance nouvellement créée du moniteur d’initialisation MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-129">[out] A pointer to receive the newly created instance of the MAPI initialization monitor.</span></span>
  
## <a name="return-values"></a><span data-ttu-id="a3e5b-130">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a3e5b-130">Return values</span></span>

<span data-ttu-id="a3e5b-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3e5b-131">S_OK</span></span>
> <span data-ttu-id="a3e5b-132">Une nouvelle instance du moniteur d’initialisation a été créée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-132">A new instance of the initialization monitor was created successfully.</span></span>

<span data-ttu-id="a3e5b-133">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="a3e5b-133">E_OUTOFMEMORY</span></span>
> <span data-ttu-id="a3e5b-134">Il n’y avait pas assez de mémoire pour un nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="a3e5b-134">There was not enough memory to crate a new object.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3e5b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3e5b-135">See also</span></span>
[<span data-ttu-id="a3e5b-136">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="a3e5b-136">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="a3e5b-137">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="a3e5b-137">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
