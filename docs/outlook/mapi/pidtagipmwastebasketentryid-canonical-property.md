---
title: Propriété canonique PidTagIpmWastebasketEntryId
description: Décrit la propriété canonique PidTagIpmWastebasketEntryId, qui contient l’identificateur d’entrée du dossier éléments supprimés IPM standard.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
ms.openlocfilehash: 38ce7ff5d131ab5df0cf8e994b4d9fc1ae25781e
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752231"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a>Propriété canonique PidTagIpmWastebasketEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier Éléments supprimés du message interpersonnel standard (IPM). 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_WASTEBASKET_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Une application cliente doit déplacer les messages interpersonnels supprimés vers le dossier Éléments supprimés. Si le message se trouve déjà dans ce dossier ou si cette propriété n’est pas prise en charge, le client doit supprimer le message. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

