---
title: Propriété canonique PidTagContentCorrelator
description: Décrit la propriété canonique PidTagContentCorrelator, qui contient une valeur que l’expéditeur du message peut utiliser pour faire correspondre un rapport au message d’origine.
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
ms.openlocfilehash: 64baf12505cbfe42dd40e6f50a9d01fd8b2a1c68
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769563"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Propriété canonique PidTagContentCorrelator

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur que l’expéditeur du message peut utiliser pour faire correspondre un rapport au message d’origine.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Identificateur :  <br/> |0x0007  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Le contenu de la chaîne binaire est défini par l’expéditeur du message. Si elle est définie sur un message sortant, cette propriété doit être copiée sur tous les rapports générés en réponse au message.
  
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

