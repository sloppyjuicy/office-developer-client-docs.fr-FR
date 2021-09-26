---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 60bfb43f99ef6831ab7dda837924a00d9c3d94a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630963"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur une case à cocher qui sera utilisée dans une boîte de dialogue conçue à partir d’un tableau d’affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de la chaîne de caractères affichée avec la case à cocher. 
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette de case à cocher. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulPRPropertyName**
  
> Balise de propriété pour une propriété de type PT_BOOLEAN. La valeur de cette propriété est affectée par l’état de la case à cocher.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLCHECKBOX** décrit une case à cocher qui reflète l’un des deux états : activé (case à cocher) ou désactivé (case vide). 
  
Le **membre ulPRPropertyName** décrit une propriété Boolean dont la valeur est manipulée en modifiant l’état de la case à cocher. Lorsque la case à cocher est affichée pour la première fois, MAPI appelle la méthode **GetProps** de l’implémentation **IMAPIProp** associée à la table d’affichage pour récupérer un ensemble de propriétés par défaut. Si l’une des propriétés est m moire à la balise de propriété dans la structure **DTBLCHECKBOX,** la valeur de cette propriété est affichée en tant que valeur initiale de la case à cocher. 
  
Les contrôles de case à cocher peuvent être modifiables. Cela permet à un utilisateur de changer d’état. Les cases à cocher modifiables définissent l’indicateur DT_EDITABLE dans le membre **ulCtlFlags** de leur structure [DTCTL](dtctl.md) et dans leur propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Lorsqu’une case à cocher change d’état, MAPI appelle [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir la propriété identifiée dans le membre de balise de propriété de la structure **DTBLCHECKBOX** sur le nouvel état. 
  
Par exemple, un fournisseur de carnet d’adresses peut inclure un contrôle de case à cocher modifiable dans sa boîte de dialogue de configuration pour ajuster le paramètre de la propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) d’un destinataire. Lorsque l’utilisateur sélectionne la case à cocher, MAPI définit cette propriété sur TRUE. Lorsque la case à cocher n’est pas cocher, la propriété est définie sur FALSE.
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md). Pour plus d’informations sur les types de propriétés, voir [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

