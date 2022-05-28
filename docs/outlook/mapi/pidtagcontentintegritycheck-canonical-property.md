---
title: Propriété canonique PidTagContentIntegrityCheck
description: Décrit la propriété canonique PidTagContentIntegrityCheck, qui fournit la non-répudiation du contenu du message.
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
ms.openlocfilehash: 79af4403adaf408c284973c0e5157ae1cb3c4cde
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769717"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Propriété canonique PidTagContentIntegrityCheck

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de vérification de l’intégrité du contenu ASN.1 qui permet à un expéditeur de messages de protéger le contenu du message contre la divulgation aux destinataires non autorisés.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Identificateur :  <br/> |0x0C00  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété permet de ne pas répudier le contenu du message. Conjointement avec **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), il garantit que le contenu d’un message arrive à sa destination inchangé.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

