---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: Décrit une étiquette qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.
ms.openlocfilehash: 07d86b6e1bd738f30dac616d84e357d8c3adcc34
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405565"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une étiquette qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Position en mémoire de l’étiquette de chaîne de caractères.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabelName** . L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLLABEL** décrit un texte de contrôle d’étiquette qui est affiché avec un autre type de contrôle pour ajouter une signification à ce contrôle. Par exemple, la plupart des contrôles d’édition sont placés à côté des étiquettes pour informer l’utilisateur du type d’informations à entrer. Certains contrôles, tels que les zones de groupe et les cases d’radio, tiennent leurs propres étiquettes. 
  
L’étiquette peut inclure un accélérateur Windows, identifié comme le caractère suivant l’eterrable (&amp;). Le fait d’appuyer sur la touche d’accélérateur met le focus sur le premier contrôle sans étiquette, nonbutton, qui suit cette étiquette dans le tableau d’affichage.
  
Il n’existe aucune prise en charge des étiquettes multilignes. L’affichage de plusieurs lignes nécessite plusieurs étiquettes.
  
Il n’est pas possible d’utiliser une étiquette comme contrôle d’édition en lecture seule. La différence est qu’un contrôle d’édition peut être sélectionné et copié alors qu’une étiquette ne le peut pas. 
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

