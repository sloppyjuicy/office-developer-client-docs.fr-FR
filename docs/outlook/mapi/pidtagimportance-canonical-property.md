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
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786098"
---
# <a name="pidtagimportance-canonical-property"></a>Propriété canonique PidTagImportance

  
  
**S’applique à**: Outlook 
  
Contient une valeur qui indique l’avis de l’expéditeur du message de l’importance d’un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPORTANCE  <br/> |
|Identificateur :  <br/> |0x0017  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété et la propriété **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondus. Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel de système de messagerie. Priorité plus élevée indique généralement un coût plus élevé. Importance supérieure est généralement associée à un autre affichage par l’interface utilisateur. 
  
Cette propriété peut avoir exactement une des valeurs suivantes :
  
IMPORTANCE_LOW 
  
> Le message a une importance faible.
    
IMPORTANCE_HIGH 
  
> Le message a une haute importance.
    
IMPORTANCE_NORMAL 
  
> Le message a importance normale.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

