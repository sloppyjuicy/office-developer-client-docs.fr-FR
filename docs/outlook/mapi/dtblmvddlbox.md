---
title: DTBLMVDDLBOX
description: DTBLMVDDLBOX décrit une liste déroulante qui sera utilisée dans une boîte de dialogue générée à partir d’une table d’affichage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
ms.openlocfilehash: 2cb07f11112e514f35f758a07cd746ff41f8ba0e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817542"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste déroulante qui sera utilisée dans une boîte de dialogue créée à partir d’une table d’affichage.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> Réservé; doit être égal à zéro.
    
 **ulMVPropTag**
  
> Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING. Les différentes valeurs de cette propriété sont affichées sous forme d’entrées distinctes dans la liste déroulante.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLMVDDLBOX** décrit une liste déroulante à valeurs multiples une liste déroulante en lecture seule d’éléments. À l’aide d’une liste déroulante à valeurs multiples, les valeurs s’affichent lorsqu’un utilisateur clique sur une barre de défilement. 
  
Les données affichées proviennent de la propriété identifiée dans le membre **ulMVPropTag** . Il n’est pas nécessaire de lire à partir de l’interface de propriété associée à la table d’affichage. En outre, étant donné que les utilisateurs ne sont pas en mesure d’effectuer des sélections à partir de ces types de zones de liste, les données ne sont pas écrites dans l’interface de propriété. 
  
Seules les propriétés de chaîne à valeurs multiples sont prises en charge pour la liste déroulante à valeurs multiples ; d’autres types de propriétés à valeurs multiples ne sont pas pris en charge. 
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

