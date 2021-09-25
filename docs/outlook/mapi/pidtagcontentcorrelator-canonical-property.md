---
title: Propriété canonique PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: baad9a247687f9753a5c63d27c7e9cdc07b74e5e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616543"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Propriété canonique PidTagContentCorrelator

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur que l’expéditeur du message peut utiliser pour faire correspondre un état au message d’origine.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Identificateur :  <br/> |0x0007  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Le contenu de la chaîne binaire est défini par l’auteur du message. Si elle est définie sur un message sortant, cette propriété doit être copiée dans tous les états générés en réponse au message.
  
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

