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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786456"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Propriété canonique PidTagProviderParentItemId

  
  
**S’applique à**: Outlook 
  
Spécifie un identificateur pour l’objet parent d’un dossier ou un élément dans une banque.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Identificateur :  <br/> |0x0EA4  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

