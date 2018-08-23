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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7449e59227b147d34c2329175d0251dbb9c427b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581341"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propriété canonique PidTagCommonViewsEntryId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier commun affichage prédéfini. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Le dossier d’affichage communs contient un ensemble prédéfini des spécificateurs d’affichage standard, tandis que le dossier d’affichage contient des spécificateurs définis par un utilisateur de messagerie. Ces dossiers, qui ne sont pas visibles dans la hiérarchie de message interpersonnel (IPM), peuvent contenir plusieurs spécificateurs d’affichage, chacune étant stockées sous forme de message. Une application cliente pouvez choisir de fusionner les deux jeux de spécificateurs et les divulguer les deux. 
  
Pour plus d’informations sur les affichages, voir [Afficher les dossiers](mapi-view-folders.md).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Propriété canonique PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

