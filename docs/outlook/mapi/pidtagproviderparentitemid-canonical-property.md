---
title: Propriété canonique PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d0ec4e793a5b7940802ee159c2e869695166ce93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563281"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Propriété canonique PidTagProviderParentItemId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie un identificateur pour l’objet parent d’un dossier ou un élément dans une banque.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Identificateur :  <br/> |0x0EA4  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Fournisseurs de magasins peuvent spécifier une valeur pour cette propriété pour un parent d’un dossier ou un élément, mais doivent conserver la valeur de la même session. Fournisseurs de magasins d’utilisent cette propriété pour identifier des résultats de recherche renvoyés à partir d’un moteur de recherche.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

