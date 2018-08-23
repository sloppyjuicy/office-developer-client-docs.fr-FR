---
title: Extension des listes de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c7c0043ed898a827b2ea8c65b20837c571f88883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582055"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="3a2a0-103">Extension des listes de distribution</span><span class="sxs-lookup"><span data-stu-id="3a2a0-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="3a2a0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a2a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3a2a0-105">**Pour demander de MAPI pour développer une liste de distribution**</span><span class="sxs-lookup"><span data-stu-id="3a2a0-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="3a2a0-106">Définissez sa propriété **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) à MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="3a2a0-107">MAPI développe les adresses de ce type avant d’envoyer le message vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

