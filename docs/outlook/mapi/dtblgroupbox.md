---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 43aeba3be0181b4e5f5a203e7d1e4d0a64ec2bbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601120"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de la chaîne de caractères qui accompagne la zone de groupe. S’il est affiché, l’étiquette apparaît en haut, à gauche de la zone.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel.** L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLGROUPBOX** décrit un contrôle de zone de groupe utilisé pour associer visuellement d’autres contrôles dans la boîte de dialogue. La technique de mise en surbrillance implique d’entourer les autres contrôles d’une zone. 
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

