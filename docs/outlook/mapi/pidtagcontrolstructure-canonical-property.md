---
title: Propriété canonique PidTagControlStructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b517888d562ee5b178dbd011fa1ce6ab218c6b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594354"
---
# <a name="pidtagcontrolstructure-canonical-property"></a>Propriété canonique PidTagControlStructure

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un pointeur vers une structure d’un contrôle utilisé dans une boîte de dialogue. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_STRUCTURE  <br/> |
|Identificateur :  <br/> |0x3F01  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Afficher une table MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété représente un pointeur de type long qui est converti à une des structures de contrôle. Les structures de contrôle sont les suivantes :
  
|||
|:-----|:-----|
|[DTBLBUTTON](dtblbutton.md) <br/> |[DTBLCHECKBOX](dtblcheckbox.md) <br/> |
|[DTBLCOMBOBOX](dtblcombobox.md) <br/> |[DTBLDDLBX](dtblddlbx.md) <br/> |
|[DTBLEDIT](dtbledit.md) <br/> |[DTBLGROUPBOX](dtblgroupbox.md) <br/> |
|[DTBLLABEL](dtbllabel.md) <br/> |[DTBLLBX](dtbllbx.md) <br/> |
|[DTBLMVDDLBOX](dtblmvddlbox.md) <br/> |[DTBLMVLISTBOX](dtblmvlistbox.md) <br/> |
|[DTBLPAGE](dtblpage.md) <br/> |[DTBLRADIOBUTTON](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

