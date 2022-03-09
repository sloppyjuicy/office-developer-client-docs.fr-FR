---
title: Accès aux membres d’une liste de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
ms.openlocfilehash: 66d975eaacf00912e7f393cc77e6929a7b7f7ec1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376342"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Accès aux membres d’une liste de distribution

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour obtenir les membres d’une liste de distribution**
  
1. Créez un tableau de balises de propriétés de taille moyenne avec les propriétés des membres que vous souhaitez récupérer, tels que **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. [Appelez IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir la liste de distribution. 
    
3. Appelez la méthode **IABContainer::GetContentsTable** de la liste de distribution pour accéder à sa table des matières. 
    
4. [Appelez HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes du tableau représentant les membres de la liste de distribution. 
    

