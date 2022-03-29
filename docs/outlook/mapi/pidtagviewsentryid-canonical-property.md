---
title: Propriété canonique PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: Contient l’identificateur d’entrée du dossier Affichages définis par l’utilisateur pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 7c9f26760c3a002cb3b56cf1f37e49618b63e7a3
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456314"
---
# <a name="pidtagviewsentryid-canonical-property"></a>Propriété canonique PidTagViewsEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier Affichages définis par l’utilisateur.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E5  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Magasin de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le dossier d’affichage commun contient un ensemble prédéféré de  specifieurs d’affichage standard, tandis que le dossier d’affichage contient des  specifieurs définis par un utilisateur de messagerie. Ces dossiers, qui ne sont pas visibles dans la hiérarchie des messages interpersonnels (IPM), peuvent contenir de nombreux  spécifiés d’affichage, chacun étant stocké sous la mesure d’un message. L’application cliente peut choisir de fusionner les deux ensembles de  specifiers et de les rendre disponibles.
  
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

