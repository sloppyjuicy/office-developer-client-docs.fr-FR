---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407213"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="c563c-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="c563c-103">MAPICrashRecovery</span></span>

<span data-ttu-id="c563c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c563c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c563c-105">La **fonction MAPICrashRecovery** vérifie l’état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST).</span><span class="sxs-lookup"><span data-stu-id="c563c-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="c563c-106">Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche tout accès en lecture ou en écriture jusqu’à ce que le processus soit terminé.</span><span class="sxs-lookup"><span data-stu-id="c563c-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c563c-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c563c-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c563c-108">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="c563c-108">Exported by:</span></span>  <br/> |<span data-ttu-id="c563c-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c563c-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c563c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c563c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c563c-111">Client</span><span class="sxs-lookup"><span data-stu-id="c563c-111">Client</span></span>  <br/> |
|<span data-ttu-id="c563c-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c563c-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c563c-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="c563c-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="c563c-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="c563c-114">Parameters</span></span>

<span data-ttu-id="c563c-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c563c-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c563c-116">[in] Indicateurs utilisés pour contrôler la façon dont la récupération d’incident MAPI est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c563c-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="c563c-117">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="c563c-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="c563c-118">**MAPICRASH \_ RECOVER**: si les PST ou osts sont dans un état cohérent, déplacez les données sur le disque et verrouillez les PST ou osts pour empêcher l’accès en lecture ou en écriture.</span><span class="sxs-lookup"><span data-stu-id="c563c-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="c563c-119">**MAPICRASH \_ CONTINUE**: Déverrouillez les PST ou osts pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="c563c-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="c563c-120">Après un appel réussi à **MAPICrashRecovery** avec l’indicateur **MAPICRASH_RECOVER,** appelez **MAPICrashRecovery** avec l’indicateur **MAPICRASH \_ CONTINUE** pour autoriser le débogage.</span><span class="sxs-lookup"><span data-stu-id="c563c-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="c563c-121">**MAPICRASH \_ SYSTEM_SHUTDOWN**: si les PST ou osts sont dans un état cohérent, déplacez les données sur le disque et verrouillez les PST ou osts pour empêcher l’accès en lecture ou en écriture.</span><span class="sxs-lookup"><span data-stu-id="c563c-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="c563c-122">Les PST ou osts ne peuvent pas être déverrouillés à l’aide **de MAPICRASH \_ CONTINUE**.</span><span class="sxs-lookup"><span data-stu-id="c563c-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="c563c-123">Doit être utilisé en combinaison avec **MAPICRASH \_ RECOVER**.</span><span class="sxs-lookup"><span data-stu-id="c563c-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c563c-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="c563c-124">Remarks</span></span>

<span data-ttu-id="c563c-125">L’byte supérieur (0xFF000000) est réservé aux indicateurs de récupération d’incident spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c563c-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="c563c-126">Appelez **MAPICrashRecovery** avec les indicateurs  **MAPICRASH_SYSTEM_SHUTDOWN MAPICRASH \_** en réponse au message **WM_ENDSESSION** message.</span><span class="sxs-lookup"><span data-stu-id="c563c-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c563c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c563c-127">See also</span></span>

- [<span data-ttu-id="c563c-128">À propos de l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="c563c-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="c563c-129">Utiliser l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="c563c-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

