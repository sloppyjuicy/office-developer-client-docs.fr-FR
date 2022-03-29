---
title: Propriété canonique PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bb4a50aa24b4a0921ee640554bbedff3cad3917f
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454893"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Propriété canonique PidTagContentIntegrityCheck

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de vérification de l’intégrité du contenu ASN.1 qui permet à un expéditeur de message de protéger le contenu du message contre la divulgation à des destinataires non autorisés.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Identificateur :  <br/> |0x0C00  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété permet de ne pas répudier le contenu des messages. Conjointement **avec PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), il garantit que le contenu d’un message arrive à sa destination inchangée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

