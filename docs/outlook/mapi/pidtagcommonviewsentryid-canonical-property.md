---
title: Propriété canonique PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331744"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propriété canonique PidTagCommonViewsEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'identificateur d'entrée du dossier d'affichage commun prédéfini. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Le dossier d'affichage commun contient un ensemble prédéfini de spécificateurs d'affichage standard, tandis que le dossier d'affichage contient des spécificateurs définis par un utilisateur de messagerie. Ces dossiers, qui ne sont pas visibles dans la hiérarchie des messages interpersonnels (IPM), peuvent contenir de nombreux spécificateurs d'affichage, chacun étant stocké sous forme de message. Une application cliente peut choisir de fusionner les deux jeux de spécificateurs et les rendre disponibles. 
  
Pour plus d'informations sur les affichages, consultez la rubrique [afficher les dossiers](mapi-view-folders.md).
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Propriété canonique PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

