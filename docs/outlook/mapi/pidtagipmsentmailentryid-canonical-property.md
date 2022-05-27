---
title: Propriété canonique PidTagIpmSentMailEntryId
description: Décrit la propriété canonique PidTagIpmSentMailEntryId, qui contient l’identificateur d’entrée du dossier Messages interpersonnels standard (IPM) Éléments envoyés.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
ms.openlocfilehash: 1d877c2d3bed2f8b6a3b54d8030a5ec3dceb13b7
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752602"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a>Propriété canonique PidTagIpmSentMailEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier Éléments envoyés du message interpersonnel standard (IPM). 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_SENTMAIL_ENTRYID  <br/> |
|Identificateur :  <br/> |0x35E4  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Une fois envoyés, les messages interpersonnels sont généralement placés dans le dossier Éléments envoyés. Un client peut utiliser cette propriété pour définir la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sur un message envoyé. 
  
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

