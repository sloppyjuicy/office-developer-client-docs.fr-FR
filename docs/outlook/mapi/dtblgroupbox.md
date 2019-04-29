---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438392"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de la chaîne de caractères qui accompagne la zone de groupe. Si elle est affichée, l'étiquette apparaît en haut à gauche de la zone.
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format de l'étiquette désignée par le membre **ulbLpszLabel** . L'indicateur suivant peut être défini: 
    
MAPI_UNICODE 
  
> L'étiquette est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLGROUPBOX** décrit un contrôle de zone de groupe qui est utilisé pour associer visuellement d'autres contrôles dans la boîte de dialogue. La technique de mise en surbrillance implique d'entourer les autres contrôles d'un cadre. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

