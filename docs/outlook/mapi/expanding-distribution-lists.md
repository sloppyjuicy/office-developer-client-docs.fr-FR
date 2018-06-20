---
title: Développer des listes de Distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 47a37683ac54bef72ebd50aaaa11a36bdfd28659
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783271"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="5d245-103">Développer des listes de Distribution</span><span class="sxs-lookup"><span data-stu-id="5d245-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="5d245-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d245-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="5d245-105">**Pour demander de MAPI pour développer une liste de distribution**</span><span class="sxs-lookup"><span data-stu-id="5d245-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="5d245-106">Définissez sa propriété **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) à MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="5d245-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="5d245-107">MAPI développe les adresses de ce type avant d’envoyer le message vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="5d245-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

