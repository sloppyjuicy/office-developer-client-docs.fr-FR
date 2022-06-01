---
title: Propriété canonique PidLidTaskFCreator
description: Décrit la propriété canonique PidLidTaskFCreator, qui indique que la tâche a été créée par l’utilisateur ou l’agent utilisateur actuel.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
ms.openlocfilehash: e2304bc304903d0f14f1a4202bf1b55601829a4b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811661"
---
# <a name="pidlidtaskfcreator-canonical-property"></a>Propriété canonique PidLidTaskFCreator

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique que la tâche a été créée à l’origine par l’utilisateur ou l’agent utilisateur actuel au lieu de traiter une demande de tâche.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskFCreator  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID long (LID) :  <br/> |0x0000811E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Le client définit cette propriété sur TRUE lorsque l’utilisateur crée la tâche et sur FALSE lorsque la tâche est affectée par un autre utilisateur. Si cette propriété n’est pas spécifiée, la valeur TRUE est supposée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour des tâches.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

