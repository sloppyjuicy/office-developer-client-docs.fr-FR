---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420744"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste déroulante qui sera utilisée dans une boîte de dialogue créée à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> MSR doit être égal à zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING. Les différentes valeurs de cette propriété sont affichées sous forme d'entrées distinctes dans la liste déroulante.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVDDLBOX** décrit une liste déroulante à valeurs multiples, une liste d'éléments en lecture seule. À l'aide d'une liste déroulante à valeurs multiples, les valeurs s'affichent lorsqu'un utilisateur clique sur une barre de défilement. 
  
Les données affichées proviennent de la propriété identifiée dans le membre **ulMVPropTag** . Il n'existe aucun besoin de lire à partir de l'interface de propriétés associée à la table d'affichage. En outre, étant donné que les utilisateurs ne peuvent pas effectuer des sélections à partir de ces types de zones de liste, les données ne sont pas écrites dans l'interface de propriété. 
  
Seules les propriétés de chaîne à valeurs multiples sont prises en charge pour la liste déroulante à valeurs multiples; les autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

