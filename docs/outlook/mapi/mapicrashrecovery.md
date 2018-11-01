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
ms.openlocfilehash: 6b07d794a8f54477c6706cb70af60f7f7ef57d49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595341"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="db958-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="db958-103">MAPICrashRecovery</span></span>

<span data-ttu-id="db958-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db958-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db958-105">La fonction **MAPICrashRecovery** vérifie que l’état du fichier de dossiers personnels (PST) ou le fichier de dossiers en mode hors connexion (OST) de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="db958-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="db958-106">Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche plu accès en lecture ou écriture jusqu'à ce que le processus est terminé.</span><span class="sxs-lookup"><span data-stu-id="db958-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="db958-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="db958-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db958-108">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="db958-108">Exported by:</span></span>  <br/> |<span data-ttu-id="db958-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="db958-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="db958-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="db958-110">Called by:</span></span>  <br/> |<span data-ttu-id="db958-111">Client</span><span class="sxs-lookup"><span data-stu-id="db958-111">Client</span></span>  <br/> |
|<span data-ttu-id="db958-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="db958-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="db958-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="db958-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="db958-114">Param�tres</span><span class="sxs-lookup"><span data-stu-id="db958-114">Parameters</span></span>

<span data-ttu-id="db958-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="db958-115">_ulFlags_</span></span>
  
> <span data-ttu-id="db958-116">[in] Indicateurs utilisés pour contrôler la façon dont la récupération après incident MAPI est effectuée.</span><span class="sxs-lookup"><span data-stu-id="db958-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="db958-117">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="db958-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="db958-118">**MAPICRASH\_récupérer**: si les fichiers pst ou ost est dans un état cohérent, déplacer les données sur le disque et verrouiller les fichiers pst ou l’OST pour empêcher l’accès en lecture ou écriture.</span><span class="sxs-lookup"><span data-stu-id="db958-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="db958-119">**MAPICRASH\_continuer**: déverrouiller les fichiers pst ou ost pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="db958-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="db958-120">Après un appel réussi à **MAPICrashRecovery** avec l’indicateur **MAPICRASH_RECOVER** , appelez **MAPICrashRecovery** avec la **MAPICRASH\_continuer** indicateur pour autoriser le débogage continuer.</span><span class="sxs-lookup"><span data-stu-id="db958-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="db958-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: si les fichiers pst ou ost est dans un état cohérent, déplacer les données sur le disque et verrouiller les fichiers pst ou l’OST pour empêcher l’accès en lecture ou écriture.</span><span class="sxs-lookup"><span data-stu-id="db958-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="db958-122">Les fichiers pst ou OST ne peut pas être déverrouillé à l’aide de **MAPICRASH\_continuer**.</span><span class="sxs-lookup"><span data-stu-id="db958-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="db958-123">Doit être utilisée en combinaison avec **MAPICRASH\_récupérer**.</span><span class="sxs-lookup"><span data-stu-id="db958-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="db958-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="db958-124">Remarks</span></span>

<span data-ttu-id="db958-125">L’octet supérieur (0xFF000000) est réservé à des indicateurs de récupération fournisseur incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="db958-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="db958-126">Appelez **MAPICrashRecovery** avec la **MAPICRASH\_récupérer** et indicateurs **MAPICRASH_SYSTEM_SHUTDOWN** en réponse au message **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="db958-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db958-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db958-127">See also</span></span>

- [<span data-ttu-id="db958-128">À propos de l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="db958-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="db958-129">Utiliser l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="db958-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

