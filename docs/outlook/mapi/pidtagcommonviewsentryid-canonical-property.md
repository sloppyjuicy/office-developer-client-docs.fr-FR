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
description: Contient l’identificateur d’entrée du dossier d’affichage commun prédéféré. Le dossier d’affichage commun contient un ensemble prédéféré de  specifieurs d’affichage standard.
ms.openlocfilehash: b7789c9d59f8869abab9dca73f3ebc069914e233
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763900"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propriété canonique PidTagCommonViewsEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier d’affichage commun prédéféré. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Outlook application  <br/> |
   
## <a name="remarks"></a>Remarques

Le dossier d’affichage commun contient un ensemble prédéféré de  specifieurs d’affichage standard, tandis que le dossier d’affichage contient des  specifieurs définis par un utilisateur de messagerie. Ces dossiers, qui ne sont pas visibles dans la hiérarchie des messages interpersonnels (IPM), peuvent contenir de nombreux  spécifiés d’affichage, chacun étant stocké sous la mesure d’un message. Une application cliente peut choisir de fusionner les deux ensembles de  specifiers et de les rendre disponibles. 
  
Pour plus d’informations sur les [affichages, voir Afficher les dossiers](mapi-view-folders.md).
  
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

