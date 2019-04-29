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
# <a name="mapicrashrecovery"></a><span data-ttu-id="1c3d2-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="1c3d2-103">MAPICrashRecovery</span></span>

<span data-ttu-id="1c3d2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c3d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c3d2-105">La fonction **MAPICrashRecovery** vérifie l'état du fichier de dossiers personnels (PST) ou de la mémoire partagée du fichier de dossiers en mode hors connexion (OST).</span><span class="sxs-lookup"><span data-stu-id="1c3d2-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="1c3d2-106">Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche l'accès en lecture ou en écriture tant que le processus n'est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1c3d2-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1c3d2-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c3d2-108">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="1c3d2-108">Exported by:</span></span>  <br/> |<span data-ttu-id="1c3d2-109">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="1c3d2-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="1c3d2-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1c3d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="1c3d2-111">Client</span><span class="sxs-lookup"><span data-stu-id="1c3d2-111">Client</span></span>  <br/> |
|<span data-ttu-id="1c3d2-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1c3d2-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c3d2-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="1c3d2-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="1c3d2-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c3d2-114">Parameters</span></span>

<span data-ttu-id="1c3d2-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c3d2-115">_ulFlags_</span></span>
  
> <span data-ttu-id="1c3d2-116">dans Indicateurs utilisés pour contrôler la manière dont la récupération d'urgence MAPI est effectuée.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="1c3d2-117">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="1c3d2-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="1c3d2-118">**MAPICRASH\_Recover**: si les fichiers PST ou OSTs sont dans un état cohérent, déplacez les données sur le disque et verrouillez les fichiers PST ou OSTs pour empêcher l'accès en lecture ou en écriture.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="1c3d2-119">**MAPICRASH\_continue**: Déverrouillez les fichiers PST ou OSTs pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="1c3d2-120">Après un appel réussi à **MAPICrashRecovery** avec l'indicateur **MAPICRASH_RECOVER** , appelez **MAPICrashRecovery** avec l' **indicateur\_MAPICRASH continue** pour autoriser le débogage.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="1c3d2-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: si les fichiers PST ou OSTs sont dans un état cohérent, déplacez les données sur le disque et verrouillez les fichiers PST ou OSTs pour empêcher l'accès en lecture ou en écriture.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="1c3d2-122">Les fichiers PST ou OSTs ne peuvent pas être déverrouillés à l'aide de **MAPICRASH\_continuer**.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="1c3d2-123">Doit être utilisé en combinaison avec **MAPICRASH\_Recover**.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1c3d2-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c3d2-124">Remarks</span></span>

<span data-ttu-id="1c3d2-125">L'octet supérieur (0xFF000000) est réservé aux indicateurs de récupération d'incidents spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="1c3d2-126">Appelez **MAPICrashRecovery** avec les **indicateurs\_MAPICRASH Recover** et **MAPICRASH_SYSTEM_SHUTDOWN** en réponse au message **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="1c3d2-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1c3d2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c3d2-127">See also</span></span>

- [<span data-ttu-id="1c3d2-128">À propos de l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="1c3d2-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="1c3d2-129">Utiliser l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="1c3d2-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

