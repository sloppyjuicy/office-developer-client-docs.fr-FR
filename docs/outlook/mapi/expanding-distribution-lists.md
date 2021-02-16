---
title: Développement des listes de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5731a35b5d570669d8606be6dd6ca1a23fb87e88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414136"
---
# <a name="expanding-distribution-lists"></a>Développement des listes de distribution

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour inciter MAPI à développer une liste de distribution**
  
- Définissez **sa PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) sur MAPIPDL.
    
    MAPI développe les adresses de ce type avant d’envoyer le message au fournisseur de transport.
    

