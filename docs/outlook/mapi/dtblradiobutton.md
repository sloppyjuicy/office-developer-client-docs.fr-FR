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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339416"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une case d'option qui fera partie d'un groupe de cases d'option. Le groupe de cases d'option est utilisé dans une boîte de dialogue qui est générée à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Position en mémoire de l'étiquette de la chaîne de caractères pour la case d'option.
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format de l'étiquette désignée par le membre **ulbLpszLabel** . L'indicateur suivant peut être défini: 
    
MAPI_UNICODE 
  
> L'étiquette est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.
    
 **ulcButtons**
  
> Nombre de boutons dans le groupe de cases d'option. Les structures **DTBLRADIOBUTTON** pour les autres boutons du groupe doivent être contenues dans des lignes successives de la table d'affichage. Chacune de ces lignes doit contenir la même valeur pour le membre **ulcButtons** . 
    
 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_LONG. La sélection initiale dans le groupe de cases d'option est basée sur la valeur initiale de cette propriété. Chaque bouton dans le groupe doit avoir **ulPropTag** défini sur la même propriété. 
    
 **lReturnValue**
  
> Numéro unique qui identifie le bouton sélectionné.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLRADIOBUTTON** décrit un bouton radio qui est associé à un groupe de boutons. Un seul bouton du groupe peut être vérifié; le fait de définir un bouton entraîne l'annulation des autres boutons du groupe. 
  
Nombre de boutons indique le nombre de cases d'option dans le groupe. Les structures des autres cases d'option du groupe doivent se trouver dans les lignes suivantes de la table d'affichage. Chacune de ces structures doit avoir la même valeur pour le nombre de boutons.
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Structures MAPI](mapi-structures.md)

