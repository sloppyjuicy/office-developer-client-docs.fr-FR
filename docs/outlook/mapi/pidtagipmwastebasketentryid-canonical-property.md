---
title: Propriété canonique PidTagIpmWastebasketEntryId
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 99cf17cae8b3e5df9211d26c8b7cae5e97881935
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723214"
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
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

