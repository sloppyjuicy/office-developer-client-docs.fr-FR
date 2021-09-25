---
title: Propriété canonique PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d4d4de75d6d001584ea5cd6d833dc85f12913081
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600399"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propriété canonique PidTagCommonViewsEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier d’affichage commun prédéféré. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Outlook application  <br/> |
   
## <a name="remarks"></a>Remarques

Le dossier d’affichage commun contient un ensemble prédéféré de specifieurs d’affichage standard, tandis que le dossier d’affichage contient des specifieurs définis par un utilisateur de messagerie. Ces dossiers, qui ne sont pas visibles dans la hiérarchie des messages interpersonnels (IPM), peuvent contenir de nombreux spécifiés d’affichage, chacun étant stocké sous la mesure d’un message. Une application cliente peut choisir de fusionner les deux ensembles de spécifiés et de les rendre disponibles. 
  
Pour plus d’informations sur les [affichages, voir Afficher les dossiers.](mapi-view-folders.md)
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Propriété canonique PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

