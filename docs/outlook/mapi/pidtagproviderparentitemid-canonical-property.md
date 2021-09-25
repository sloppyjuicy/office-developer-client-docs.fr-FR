---
title: Propriété canonique PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a0c8af1cc36fe7f3e4c97023381e0036fed18ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574817"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Propriété canonique PidTagProviderParentItemId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un identificateur pour le parent d’un dossier ou d’un élément dans une boutique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Identificateur :  <br/> |0x0EA4  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Les fournisseurs du Store peuvent spécifier une valeur pour cette propriété pour un parent d’un dossier ou d’un élément, mais doivent conserver la même valeur entre les sessions. Les fournisseurs du Store utilisent cette propriété pour identifier les résultats de recherche renvoyés par un moteur de recherche.
  
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

