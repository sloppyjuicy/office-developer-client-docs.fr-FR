---
title: Synchronisation du texte et la mise en forme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 40d7a45ab97e0d2f8e9d3db1e1d38eb3bdb75158
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787333"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="ea9da-103">Synchronisation du texte et la mise en forme</span><span class="sxs-lookup"><span data-stu-id="ea9da-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="ea9da-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea9da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea9da-105">Le défi principal de l’envoi de messages RTF (RICH Text Format) consiste à maintenir la synchronisation avec la mise en forme du texte.</span><span class="sxs-lookup"><span data-stu-id="ea9da-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="ea9da-106">Pour garantir que lorsque les messages arrivent à destination qu’ils sont en tant que leurs auteurs prévus et que le texte et la mise en forme sont synchronisées, MAPI fournit la fonction [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="ea9da-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="ea9da-107">**RTFSync** est généralement appelée par les clients prenant en charge les RTF avant d’afficher les messages entrants et par le spouleur MAPI lorsqu’il télécharge des messages à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ea9da-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="ea9da-108">Les appelants spécifier la zone d’incohérence possible en transmettant un ou deux indicateurs à **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="ea9da-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="ea9da-109">RTF_SYNC_BODY_CHANGED pour indiquer une modification dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="ea9da-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="ea9da-110">RTF_SYNC_RTF_CHANGED pour indiquer une modification dans la mise en forme du message.</span><span class="sxs-lookup"><span data-stu-id="ea9da-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="ea9da-111">Le processus de synchronisation qui se produit dans **RTFSync** est un contrôle de redondance cyclique sophistiquées (CRC) du texte des messages qui ignore certains caractères et convertit d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="ea9da-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="ea9da-112">Caractères probablement ont été ajoutés par les fournisseurs de transport sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="ea9da-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="ea9da-113">MAPI définit plusieurs propriétés pour travailler avec le format RTF comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ea9da-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="ea9da-114">**Propriété RTF**</span><span class="sxs-lookup"><span data-stu-id="ea9da-114">**RTF property**</span></span>|<span data-ttu-id="ea9da-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ea9da-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea9da-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ea9da-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ea9da-117">Indique le début du texte du message réel.</span><span class="sxs-lookup"><span data-stu-id="ea9da-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="ea9da-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ea9da-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ea9da-119">Contient le résultat de la vérification de redondance cyclique du texte du message.</span><span class="sxs-lookup"><span data-stu-id="ea9da-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="ea9da-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ea9da-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ea9da-121">Contient le nombre de caractères dans **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="ea9da-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="ea9da-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ea9da-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ea9da-123">Valeur TRUE lorsque le message texte et la mise en forme ont été synchronisés.</span><span class="sxs-lookup"><span data-stu-id="ea9da-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="ea9da-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ea9da-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ea9da-125">Contient le nombre de caractères nonwhitespace que précédez le texte du message.</span><span class="sxs-lookup"><span data-stu-id="ea9da-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="ea9da-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ea9da-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ea9da-127">Contient le nombre de caractères nonwhitespace qui trace le texte du message.</span><span class="sxs-lookup"><span data-stu-id="ea9da-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

