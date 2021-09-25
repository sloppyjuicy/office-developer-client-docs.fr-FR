---
title: Développement des listes de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0d0bd0780d8148346e7a18017f0d66d672b16ac9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601057"
---
# <a name="expanding-distribution-lists"></a>Développement des listes de distribution

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour inciter MAPI à développer une liste de distribution**
  
- Définissez **sa PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) sur MAPIPDL.
    
    MAPI développe les adresses de ce type avant d’envoyer le message au fournisseur de transport.
    

