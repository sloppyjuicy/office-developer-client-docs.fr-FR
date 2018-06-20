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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9295c37a46d3566089f708aaaa0b9fc3b5f30db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783232"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**S’applique à**: Outlook 
  
Décrit un contrôle de zone de groupe qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe :  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Membres

 **ulbLpszLabel**
  
> Position dans la mémoire de la chaîne de caractères qui accompagne la zone de groupe. Si affiché, l’étiquette s’affiche sur le côté supérieur gauche de la boîte.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabel** . Vous pouvez définir l’indicateur suivant : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLGROUPBOX** décrit un contrôle de zone de groupe qui permet d’associer visuellement des autres contrôles dans la boîte de dialogue. Mise en surbrillance repose entourant les autres contrôles à une zone. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

