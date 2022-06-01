---
title: DTBLGROUPBOX
description: DTBLGROUPBOX décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue créée à partir d’une table d’affichage.
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
ms.openlocfilehash: ecaa4a68a39dad7b19bf2a28b1466c947e2a1f7f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817549"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue créée à partir d’une table d’affichage.
  
|Propriété|Valeur|
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
  
> Position en mémoire de la chaîne de caractères qui accompagne la zone de groupe. S’il s’affiche, l’étiquette s’affiche sur le côté supérieur gauche de la zone.
    
 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel** . L’indicateur suivant peut être défini : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, l’étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLGROUPBOX** décrit un contrôle de zone de groupe utilisé pour associer visuellement d’autres contrôles dans la boîte de dialogue. La technique de mise en surbrillance implique d’entourer les autres contrôles d’une zone. 
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

