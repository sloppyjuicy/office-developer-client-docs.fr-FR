---
title: PidTagImportance Canonical, propriété
description: Décrit la propriété canonique PidTagImportance, qui contient une valeur qui indique l’opinion de l’expéditeur du message sur l’importance d’un message.
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
ms.openlocfilehash: 139f229e1f80ec0aee4d3c45ea772e3ae00bff50
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752266"
---
# <a name="pidtagimportance-canonical-property"></a>PidTagImportance Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique l’opinion de l’expéditeur du message sur l’importance d’un message. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPORTANCE  <br/> |
|Identificateur :  <br/> |0x0017  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété et la propriété **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondues. L’importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel du système de messagerie. Une priorité plus élevée indique généralement un coût plus élevé. Une importance plus élevée est généralement associée à un affichage différent par l’interface utilisateur. 
  
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
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

