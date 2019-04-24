---
title: Propriété canonique PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355614"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propriété canonique PidTagRemoteValidateOk

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient la valeur TRUE si la visionneuse à distance est autorisée à appeler la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificateur :  <br/> |0x3E0D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété apparaît dans le tableau d'État et offre un contrôle sur les performances de transport. Il peut être considéré comme une autre façon de diriger la visionneuse à distance vers inactif. Lorsqu'il est défini sur TRUE, l'afficheur à distance peut appeler **IMAPIStatus:: ValidateState** aussi souvent que vous le souhaitez. La valeur FALSe indique que l'afficheur à distance ne peut plus passer d'appels. 
  
Le fournisseur de transport définit généralement cette propriété de manière dynamique, en définissant la valeur sur FALSe pour désactiver les appels supplémentaires lorsque le fournisseur de transport dispose d'une quantité suffisante de traitement à effectuer. Lorsque le fournisseur de transport est effectué, il définit la valeur sur TRUE pour permettre à l'application cliente d'effectuer d'autres **IMAPIStatus:: ValidateState** . 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

