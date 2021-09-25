---
title: Propriété canonique PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d91720bc2e612345cff4221dbdd9c41a45b149e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587663"
---
# <a name="pidtagimportance-canonical-property"></a>Propriété canonique PidTagImportance

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique l’avis de l’expéditeur du message sur l’importance d’un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPORTANCE  <br/> |
|Identificateur :  <br/> |0x0017  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété et la **propriété PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondues. Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse d’envoi du message par le logiciel système de messagerie. Une priorité plus élevée indique généralement un coût plus élevé. Une importance plus élevée est généralement associée à un affichage différent par l’interface utilisateur. 
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
IMPORTANCE_LOW 
  
> Le message a une faible importance.
    
IMPORTANCE_HIGH 
  
> Le message a une importance élevée.
    
IMPORTANCE_NORMAL 
  
> Le message a une importance normale.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

