---
title: Développement des listes de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
ms.openlocfilehash: 4774bc525bce384e5c44967f07890248e0f3fdf1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376923"
---
# <a name="expanding-distribution-lists"></a>Développement des listes de distribution

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour inciter MAPI à développer une liste de distribution**
  
- Définissez **PR_ADDRTYPE** propriété ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) sur MAPIPDL.
    
    MAPI développe les adresses de ce type avant d’envoyer le message au fournisseur de transport.
    

