---
title: DTBLRADIOBUTTON
description: DTBLRADIOBUTTON décrit une case d’option qui fera partie d’un groupe de boutons d’option, qui sera utilisée dans une boîte de dialogue générée à partir d’une table d’affichage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
ms.openlocfilehash: 9b3b2c90287c2390793e4c58df8fbcaf76a754d2
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815876"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une case d’option qui fera partie d’un groupe de cases d’option. Le groupe de cases d’option est utilisé dans une boîte de dialogue créée à partir d’une table d’affichage.
  
|Propriété |Valeur |
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
  
> Position en mémoire de l’étiquette de chaîne de caractères pour la case d’option.
    
 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel** . L’indicateur suivant peut être défini : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, l’étiquette est au format ANSI.
    
 **ulcButtons**
  
> Nombre de boutons dans le groupe de cases d’option. Les structures **DTBLRADIOBUTTON** des autres boutons du groupe doivent être contenues dans les lignes successives de la table d’affichage. Chacune de ces lignes doit contenir la même valeur pour le membre **ulcButtons** . 
    
 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_LONG. La sélection initiale dans le groupe de cases d’option est basée sur la valeur initiale de cette propriété. **UlPropTag** doit être défini sur la même propriété pour chaque bouton du groupe. 
    
 **lReturnValue**
  
> Numéro unique qui identifie le bouton sélectionné.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLRADIOBUTTON** décrit une case d’option d’un contrôle de bouton associé à un groupe de boutons. Un seul bouton du groupe peut être vérifié ; si vous définissez un bouton, les autres boutons du groupe ne sont pas définis. 
  
Le nombre de boutons est le nombre de cases d’option dans le groupe. Les structures des autres cases d’option du groupe doivent se trouver dans les lignes suivantes de la table d’affichage. Chacune de ces structures doit avoir la même valeur pour son nombre de boutons.
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Structures MAPI](mapi-structures.md)

