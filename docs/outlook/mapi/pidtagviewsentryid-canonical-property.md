---
title: Propriété canonique PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786903"
---
# <a name="pidtagviewsentryid-canonical-property"></a>Propriété canonique PidTagViewsEntryId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée du dossier vues définies par l’utilisateur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E5  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le dossier d’affichage communs contient un ensemble prédéfini des spécificateurs d’affichage standard, tandis que le dossier d’affichage contient des spécificateurs définis par un utilisateur de messagerie. Ces dossiers, qui ne sont pas visibles dans la hiérarchie de message interpersonnel (IPM), peuvent contenir plusieurs spécificateurs d’affichage, chacune étant stockées sous forme de message. La possibilité de l’application cliente à fusionner les deux jeux de spécificateurs et les divulguer les deux.
  
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

