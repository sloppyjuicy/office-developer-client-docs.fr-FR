---
title: Propriété canonique PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: Contient le nom complet du dossier dans lequel un message a été trouvé au cours d’une recherche. Ces propriétés apparaissent uniquement dans la table des matières d’un dossier de résultats de recherche.
ms.openlocfilehash: d4e1cbff80358c3f56511b39101227f5f1608903
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524338"
---
# <a name="pidtagparentdisplay-canonical-property"></a>Propriété canonique PidTagParentDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet du dossier dans lequel un message a été trouvé au cours d’une recherche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W  <br/> |
|Identificateur :  <br/> |0x0E05  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés ne se trouve sur aucun objet. Elles peuvent uniquement apparaître dans la table des matières d’un dossier de résultats de recherche.
  
Ces propriétés **et PR_PARENT_ENTRYID** propriétés ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) ne sont pas liées les unes aux autres. Ils appartiennent à des contextes totalement différents.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

