---
title: Accès aux membres d’une liste de Distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782881"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Accès aux membres d’une liste de Distribution

  
  
**S’applique à**: Outlook 
  
 **Pour obtenir les membres d’une liste de distribution**
  
1. Créer un tableau de balise de propriété ajustés avec les propriétés des membres que vous souhaitez récupérer, comme **PR_DISPLAY_TYPE** ([ , **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir la liste de distribution. 
    
3. Appelez la méthode **IABContainer::GetContentsTable** de la liste de distribution pour accéder à sa table des matières. 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes de la table qui représente les membres de la liste de distribution. 
    

