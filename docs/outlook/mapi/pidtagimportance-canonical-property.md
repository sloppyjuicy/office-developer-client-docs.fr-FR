---
title: Propriété canonique PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327922"
---
# <a name="pidtagimportance-canonical-property"></a>Propriété canonique PidTagImportance

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique l'importance d'un message pour l'expéditeur du message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPORTANCE  <br/> |
|Identificateur :  <br/> |0x0017  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété et la propriété **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondues. Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l'ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel du système de messagerie. Une priorité élevée indique généralement un coût supérieur. Une importance plus élevée est généralement associée à un affichage différent par l'interface utilisateur. 
  
Cette propriété peut avoir exactement l'une des valeurs suivantes:
  
IMPORTANCE_LOW 
  
> Le message a une importance faible.
    
IMPORTANCE_HIGH 
  
> Le message a une importance haute.
    
IMPORTANCE_NORMAL 
  
> Le message a une importance normale.
    
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

