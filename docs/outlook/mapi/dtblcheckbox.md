---
title: DTBLCHECKBOX
description: DTBLCHECKBOX contient des informations sur une case à cocher qui sera utilisée dans une boîte de dialogue créée à partir d’une table d’affichage.
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
ms.openlocfilehash: 7bf12b2dac83c43359267a753119a796bef66ba4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811787"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur une case à cocher qui sera utilisée dans une boîte de dialogue créée à partir d’une table d’affichage. 
  
|Propriété |Valeur |
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
  
> Masque de bits des indicateurs utilisés pour désigner le format de l’étiquette de case à cocher. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, l’étiquette est au format ANSI.
    
 **ulPRPropertyName**
  
> Balise de propriété pour une propriété de type PT_BOOLEAN. La valeur de cette propriété est affectée par l’état de la case à cocher.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLCHECKBOX** décrit une case à cocher d’un contrôle qui reflète l’un des deux états suivants : activé (une case à cocher) ou désactivé (une case vide). 
  
Le membre **ulPRPropertyName** décrit une propriété booléenne dont la valeur est manipulée en modifiant l’état de la case à cocher. Lorsque la case à cocher s’affiche pour la première fois, MAPI appelle la méthode **GetProps** de l’implémentation **IMAPIProp** associée à la table d’affichage pour récupérer un ensemble de propriétés par défaut. Si l’une des propriétés est mappée à la balise de propriété dans la structure **DTBLCHECKBOX** , la valeur de cette propriété s’affiche comme valeur initiale de la case à cocher. 
  
Les contrôles de case à cocher peuvent être modifiables. Cela permet à un utilisateur de modifier son état. Les cases à cocher modifiables définissent l’indicateur DT_EDITABLE dans le membre **ulCtlFlags** de leur structure [DTCTL](dtctl.md) et dans leur **propriété PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Lorsqu’une case à cocher change d’état, MAPI appelle [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir la propriété identifiée dans le membre de balise de propriété de la structure **DTBLCHECKBOX** sur le nouvel état. 
  
Par exemple, un fournisseur de carnet d’adresses peut inclure un contrôle de case à cocher modifiable dans sa boîte de dialogue de configuration pour ajuster le paramètre de la propriété **PR_SEND_RICH_INFO** d’un destinataire ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Lorsque l’utilisateur active la case à cocher, MAPI définit cette propriété sur TRUE. Lorsque la case à cocher n’est pas sélectionnée, la propriété est définie sur FALSE.
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md). Pour plus d’informations sur les types de propriétés, consultez [vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

