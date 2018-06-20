---
title: Affichage de la boîte de dialogue adresse
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783207"
---
# <a name="displaying-the-common-address-dialog-box"></a>Affichage de la boîte de dialogue adresse

  
  
**S’applique à**: Outlook 
  
La boîte de dialogue adresse MAPI courantes pouvant servir à diverses tâches adressage telles que la création d’une liste de destinataires. Pour afficher cette boîte de dialogue, appelez **IAddrBook::Address**. Selon parmi les nombreux paramètres que vous définissez et la façon dont vous les définissez, vous pouvez limiter l’affichage aux entrées d’un type particulier à partir d’un conteneur spécifique.
  
 **Pour limiter la boîte de dialogue adresse à l’affichage des entrées de carnet d’adresses personnel uniquement**
  
1. Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’adresses personnel. 
    
2. Créer une restriction de propriété qui utilise RELOP_EQ pour le membre de la structure [SPropertyRestriction](spropertyrestriction.md) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) **relop** en tant que le membre **ulPropTag** . Si vous utilisez **PR_ENTRYID**, transmettez l’identificateur d’entrée est recherché dans **GetPAB**. Si vous utilisez **PR_AB_PROVIDER_ID**, passez la valeur incluse dans le MSPAB. Fichier d’en-tête H. **PR_AB_PROVIDER_ID** est l’identificateur unique pour le carnet d’adresses personnel conçu par MAPI. 
    
3. Appelez [IAddrBook::Address](iaddrbook-address.md) avec le paramètre _lpHierRestriction_ en pointant sur la restriction de propriété. 
    

