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
ms.openlocfilehash: 376f3cfb6c39720be5efd46c87265f5348529350
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524455"
---
# <a name="pidtagimportance-canonical-property"></a>Propriété canonique PidTagImportance

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique l’avis de l’expéditeur du message sur l’importance d’un message. 
  
|Propriété|Valeur|
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
  
> Le message a une importance particulière.
    
IMPORTANCE_NORMAL 
  
> Le message a une importance normale.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
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

