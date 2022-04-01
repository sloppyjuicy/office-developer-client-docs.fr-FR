---
title: Propriété canonique PidTagRemoteProgressText
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemoteProgressText
api_type:
- COM
ms.assetid: b74d4350-4ad6-4c3f-8326-bd28537dfa0f
description: Cette propriété contient une chaîne qui indique l’état d’un transfert à distance. Un code numérique associé à ce texte est transmis dans la PR_REMOTE_PROGRESS de texte.
ms.openlocfilehash: 309acb231ca604e73009cd7a237166bd797db23b
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523672"
---
# <a name="pidtagremoteprogresstext-canonical-property"></a>Propriété canonique PidTagRemoteProgressText

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient une chaîne qui indique l’état d’un transfert à distance.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_PROGRESS_TEXT, PR_REMOTE_PROGRESS_TEXT_A, PR_REMOTE_PROGRESS_TEXT_W  <br/> |
|Identificateur :  <br/> |0x3E0C  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un code numérique associé à ce texte est transmis dans la propriété **PR_REMOTE_PROGRESS** ([PidTagRemoteProgress](pidtagremoteprogress-canonical-property.md)).
  
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

