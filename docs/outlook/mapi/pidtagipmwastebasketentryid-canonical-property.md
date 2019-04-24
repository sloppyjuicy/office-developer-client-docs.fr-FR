---
title: Propriété canonique PidTagIpmWastebasketEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3794386c4461c90f973e4028132cb8220dfaa19b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327858"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a>Propriété canonique PidTagIpmWastebasketEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'identificateur d'entrée du dossier éléments supprimés de message de messagerie interpersonne (IPM) standard. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_WASTEBASKET_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Une application cliente doit déplacer les messages interpersonnels supprimés vers le dossier éléments supprimés. Si le message est déjà dans ce dossier, ou si cette propriété n'est pas prise en charge, le client doit supprimer le message. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

