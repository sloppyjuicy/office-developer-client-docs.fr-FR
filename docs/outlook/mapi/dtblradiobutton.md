---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434598"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une seule bouton d’radio qui fera partie d’un groupe de boutons d’radio. Le groupe de boutons d’radio sera utilisé dans une boîte de dialogue qui est conçue à partir d’une table d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de l’étiquette de chaîne de caractères de la bouton d’radio.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel.** L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulcButtons**
  
> Nombre de boutons dans le groupe de boutons d’radio. Les structures **DTBLRADIOBUTTON pour** les autres boutons du groupe doivent être contenues dans des lignes successives du tableau d’affichage. Chacune de ces lignes doit contenir la même valeur pour le **membre ulcButtons.** 
    
 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_LONG. La sélection initiale dans le groupe de boutons d’radio est basée sur la valeur initiale de cette propriété. Chaque bouton du groupe doit avoir **ulPropTag** définie sur la même propriété. 
    
 **lReturnValue**
  
> Numéro unique qui identifie le bouton sélectionné.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLRADIOBUTTON** décrit une bouton d’radio un contrôle de bouton associé à un groupe de boutons. Un seul bouton du groupe peut être vérifié . la définition d’un bouton entraîne l’insé« unset » des autres boutons du groupe. 
  
Le nombre de boutons est le nombre de boutons d’radio dans le groupe. Les structures des autres boutons d’radio du groupe doivent se trouver dans les lignes suivantes du tableau d’affichage. Chacune de ces structures doit avoir la même valeur pour son nombre de boutons.
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Structures MAPI](mapi-structures.md)

