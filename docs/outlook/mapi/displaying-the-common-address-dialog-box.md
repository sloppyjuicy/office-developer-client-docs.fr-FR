---
title: Affichage de la boîte de dialogue adresse commune
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337092"
---
# <a name="displaying-the-common-address-dialog-box"></a>Affichage de la boîte de dialogue adresse commune

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La boîte de dialogue adresse commune MAPI peut être utilisée pour diverses tâches d'adressage telles que la création d'une liste de destinataires. Pour afficher cette boîte de dialogue, appelez **IAddrBook:: Address**. Selon le nombre de paramètres que vous définissez et la façon dont vous les définissez, vous pouvez limiter l'affichage aux entrées d'un type particulier à partir d'un conteneur particulier.
  
 **Pour limiter la boîte de dialogue d'adresses à l'affichage des entrées du carnet d'adresses personnel uniquement**
  
1. Appelez [IAddrBook:: GetPAB](iaddrbook-getpab.md) pour récupérer l'identificateur d'entrée du PAB. 
    
2. Créez une restriction de propriété qui utilise RELOP_EQ pour le membre **RELOP** de la structure [SPropertyRestriction](spropertyrestriction.md) et soit **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), soit **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) comme membre **ulPropTag** . Si vous utilisez **PR_ENTRYID**, transmettez l'identificateur d'entrée extrait de **GetPAB**. Si vous utilisez **PR_AB_PROVIDER_ID**, transmettez la valeur incluse dans le MSPAB. Fichier d'en-tête H. **PR_AB_PROVIDER_ID** est l'identificateur unique du carnet d'adresse (PAB) conçu par MAPI. 
    
3. Appelez [IAddrBook:: Address](iaddrbook-address.md) avec le paramètre _lpHierRestriction_ pointant vers la restriction de propriété. 
    

