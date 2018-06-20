---
title: Propriété canonique PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786407"
---
# <a name="pidtagparentdisplay-canonical-property"></a>Propriété canonique PidTagParentDisplay

  
  
**S’applique à**: Outlook 
  
Contient le nom complet du dossier dans lequel un message a été trouvé pendant une recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W  <br/> |
|Identificateur :  <br/> |0x0E05  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés n’est pas sur tous les objets. Ils peuvent uniquement apparaître dans la table des matières d’un dossier de résultats de recherche.
  
Ces propriétés et les propriétés **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) ne sont pas liées à l’autre. Ils appartiennent aux contextes totalement différents.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

