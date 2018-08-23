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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9b06ebbe8cb162d77d60cfffa866438567c84c27
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576833"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propriété canonique PidTagRemoteValidateOk

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette propriété contient la valeur TRUE si la visionneuse à distance est autorisée à appeler la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificateur :  <br/> |0x3E0D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’affiche dans la table d’état et permet de contrôler les performances de transport. Il peut être considéré comme un autre moyen de diriger la visionneuse distante inactif. Lorsqu’elle est définie sur TRUE, la visionneuse à distance peut appeler **IMAPIStatus::ValidateState** aussi souvent que souhaité. La valeur FALSE indique que la visionneuse distante ne peut pas émettre des appels plus. 
  
Le fournisseur de transport affecte généralement cette propriété dynamiquement, en définissant la valeur sur FALSE pour désactiver les appels lorsque le fournisseur de transport a suffisamment de traitement à exécuter. Lorsque le fournisseur de transport est terminé, il définit la valeur sur TRUE pour autoriser l’application cliente à effectuer d’autres appels **IMAPIStatus::ValidateState** . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

