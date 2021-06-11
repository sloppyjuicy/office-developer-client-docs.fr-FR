---
title: Synchronisation du texte et de la mise en forme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435102"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="47773-103">Synchronisation du texte et de la mise en forme</span><span class="sxs-lookup"><span data-stu-id="47773-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="47773-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47773-105">Le principal défi lors de l’envoi de messages au format RTF (Rich Text Format) est de maintenir le texte synchronisé avec la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="47773-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="47773-106">Pour s’assurer que lorsque les messages arrivent à destination, ils sont comme prévu par leurs créateurs et que le texte et la mise en forme sont synchronisés, MAPI fournit la [fonction RTFSync.](rtfsync.md)</span><span class="sxs-lookup"><span data-stu-id="47773-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="47773-107">**RtFSync** est généralement appelé par les clients rtF avant d’afficher les messages entrants et par lepooler MAPI lorsqu’il télécharge les messages vers un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="47773-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="47773-108">Les appelants spécifient la zone de incohérence possible en passant un ou deux indicateurs à **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="47773-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="47773-109">RTF_SYNC_BODY_CHANGED pour indiquer une modification dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="47773-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="47773-110">RTF_SYNC_RTF_CHANGED pour indiquer une modification dans la mise en forme des messages.</span><span class="sxs-lookup"><span data-stu-id="47773-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="47773-111">Le processus de synchronisation qui se produit dans **RTFSync** est une vérification sophistiquée de la redondance cyclique (CRC) du texte du message qui ignore certains caractères et en convertit d’autres.</span><span class="sxs-lookup"><span data-stu-id="47773-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="47773-112">Les caractères qui ont probablement été ajoutés par les fournisseurs de transport sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="47773-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="47773-113">MAPI définit plusieurs propriétés pour travailler avec rtf comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="47773-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="47773-114">**RtF, propriété**</span><span class="sxs-lookup"><span data-stu-id="47773-114">**RTF property**</span></span>|<span data-ttu-id="47773-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="47773-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47773-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47773-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="47773-117">Indique le début du texte du message réel.</span><span class="sxs-lookup"><span data-stu-id="47773-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="47773-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47773-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="47773-119">Contient le résultat de la vérification de redondance cyclique du texte du message.</span><span class="sxs-lookup"><span data-stu-id="47773-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="47773-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47773-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="47773-121">Contient le nombre de caractères dans **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="47773-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="47773-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47773-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="47773-123">Valeur TRUE lorsque le texte et la mise en forme du message ont été synchronisés.</span><span class="sxs-lookup"><span data-stu-id="47773-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="47773-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47773-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="47773-125">Contient le nombre de caractères nonwhitespace qui ont précédé le texte du message.</span><span class="sxs-lookup"><span data-stu-id="47773-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="47773-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47773-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="47773-127">Contient le nombre de caractères nonwhitespace qui s’ajoutent au texte du message.</span><span class="sxs-lookup"><span data-stu-id="47773-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

