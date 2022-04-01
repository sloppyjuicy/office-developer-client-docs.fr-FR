---
title: Propriété canonique PidTagIpmSentMailEntryId
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 085b3f1a133cd564ea25f035735ea7a77b3af1a3
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524478"
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
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

