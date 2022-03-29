---
title: Propriété canonique PidTagControlStructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ec365abdce339f2e1c1aa34c6ee01527cfce3d25
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455138"
---
# <a name="pidtagcontrolstructure-canonical-property"></a>Propriété canonique PidTagControlStructure

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un pointeur vers une structure pour un contrôle utilisé dans une boîte de dialogue. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_STRUCTURE  <br/> |
|Identificateur :  <br/> |0x3F01  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Tableau d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété représente un pointeur long qui est casté vers l’une des structures de contrôle. Les structures de contrôle sont les suivantes :
  
|Structure des contrôles|Structure du contrôle (suite)|
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
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

