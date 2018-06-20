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
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783235"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**S’applique à**: Outlook 
  
Décrit une case d’option doit faire partie d’un groupe de boutons radio. Le groupe de boutons radio permettra dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.
  
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

## <a name="members"></a>Membres

 **ulbLpszLabel**
  
> Position dans la mémoire de l’étiquette de chaîne de caractères pour le bouton d’option.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabel** . Vous pouvez définir l’indicateur suivant : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulcButtons**
  
> Nombre de boutons dans le groupe de boutons radio. Les structures **DTBLRADIOBUTTON** pour les autres boutons dans le groupe doivent être contenues dans les lignes de la table d’affichage. Chacune de ces lignes doit contenir la même valeur pour le membre **ulcButtons** . 
    
 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_LONG. La sélection dans le groupe de bouton radio initiale est basée sur la valeur initiale de cette propriété. Chaque bouton dans le groupe doit avoir **ulPropTag** à la même propriété. 
    
 **lReturnValue**
  
> Numéro unique qui identifie le bouton sélectionné.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLRADIOBUTTON** décrit une case d’option un contrôle bouton qui est associé à un groupe de boutons. Seul le bouton dans le groupe peut être archivé ; un bouton provoque les autres boutons dans le groupe est annulée. 
  
Le nombre de bouton est le nombre de cases d’option dans le groupe. Les structures pour les autres cases dans le groupe doivent être dans les lignes suivantes dans le tableau d’affichage. Chacun de ces structures doit avoir la même valeur pour le nombre de boutons.
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Structures MAPI](mapi-structures.md)

