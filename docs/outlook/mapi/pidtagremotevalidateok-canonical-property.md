---
title: Propriété canonique PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: Cette propriété contient TRUE si la visionneuse distante est autorisée à appeler la méthode IMAPIStatus::ValidateState.
ms.openlocfilehash: 6a2e754dbe7e217cc4765a5d940538f4beb636bd
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763403"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propriété canonique PidTagRemoteValidateOk

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient TRUE si la visionneuse distante est autorisée à appeler la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificateur :  <br/> |0x3E0D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété apparaît dans le tableau d’état et offre un certain contrôle sur les performances de transport. Il peut être considéré comme un autre moyen de diriger la visionneuse à distance vers l’inactivité. Lorsqu’elle est définie sur TRUE, la visionneuse distante peut appeler **IMAPIStatus::ValidateState** aussi souvent que vous le souhaitez. La valeur FALSE indique que la visionneuse distante ne peut plus effectuer d’appels. 
  
En règle générale, le fournisseur de transport définit cette propriété dynamiquement, en lui activant la valeur FALSE pour désactiver les appels supplémentaires lorsque le fournisseur de transport dispose d’un volume de traitement suffisant. Une fois le fournisseur de transport terminé, il définit la valeur sur TRUE pour permettre à l’application cliente d’effectuer d’autres **appels IMAPIStatus::ValidateState** . 
  
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

