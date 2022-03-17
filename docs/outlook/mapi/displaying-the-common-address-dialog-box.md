---
title: Affichage de la boîte de dialogue Adresse commune
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
ms.openlocfilehash: 439128a815e5398d97f1568e36a95824acb579ac
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519901"
---
# <a name="displaying-the-common-address-dialog-box"></a>Affichage de la boîte de dialogue Adresse commune

**S’applique à** : Outlook 2013 | Outlook 2016
  
La boîte de dialogue d’adresse commune MAPI peut être utilisée pour diverses tâches d’adressa ment, telles que la construction d’une liste de destinataires. Pour afficher cette boîte de dialogue, appelez **IAddrBook::Address**. En fonction du nombre de paramètres que vous définissez et de la façon dont vous les définissez, vous pouvez limiter votre affichage aux entrées d’un type particulier à partir d’un conteneur particulier.
  
 **Pour limiter la boîte de dialogue d’adresses à l’affichage des entrées de carnet d’adresses personnels uniquement**
  
1. [Appelez IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’identité.

2. Créez une restriction de propriété qui utilise RELOP_EQ pour le membre **relop** de la structure [SPropertyRestriction](spropertyrestriction.md) et **PR_ENTRYID (**[PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) en tant que membre **ulPropTag**. Si vous utilisez **PR_ENTRYID**, passez l’identificateur d’entrée récupéré à partir de **GetPAB**. Si vous utilisez **PR_AB_PROVIDER_ID**, passez la valeur incluse dans le MSPAB. Fichier d’en-tête H. **PR_AB_PROVIDER_ID** est l’identificateur unique du PAB conçu par MAPI.

3. [Appelez IAddrBook::Address](iaddrbook-address.md) avec le _paramètre lpHierRestriction_ pointant vers la restriction de propriété.
