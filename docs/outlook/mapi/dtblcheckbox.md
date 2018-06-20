---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783210"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**S’applique à**: Outlook 
  
Contient des informations sur une case à cocher qui sera utilisée dans une boîte de dialogue établie à partir d’un tableau d’affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe :  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Membres

 **ulbLpszLabel**
  
> Position dans la mémoire de la chaîne de caractères qui est affichée avec la case à cocher. 
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette de la case à cocher. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulPRPropertyName**
  
> Balise de propriété pour une propriété de type PT_BOOLEAN. La valeur de cette propriété est affectée à l’état de la case à cocher.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLCHECKBOX** décrit une case à cocher un contrôle qui reflète un des deux états : activée (une case activée) ou désactivée (une zone vide). 
  
Le membre **ulPRPropertyName** décrit une propriété booléenne dont la valeur est définie en modifiant l’état de la case à cocher. Lorsque la case à cocher s’affiche tout d’abord, MAPI appelle la méthode **GetProps** de l’implémentation **IMAPIProp** qui est associée à la table d’affichage pour récupérer un jeu de propriétés par défaut. Si une des propriétés correspond à la balise de propriété dans la structure **DTBLCHECKBOX** , la valeur de cette propriété est affichée en tant que valeur initiale de la case à cocher. 
  
Contrôles de case à cocher peuvent être modifiables. Cela permet à un utilisateur de modifier leur état. Les cases à cocher modifiables définir l’indicateur DT_EDITABLE dans le membre **ulCtlFlags** de leur structure [DTCTL](dtctl.md) et leur propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Lorsqu’une case à cocher change son état, MAPI appelle [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir la propriété identifiée dans le membre de balise de propriété de la structure **DTBLCHECKBOX** dans un nouvel état. 
  
Par exemple, un fournisseur de carnet d’adresses peut contenir un contrôle de case à cocher modifiable dans la boîte de dialogue de configuration pour régler le paramètre de propriété de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) d’un destinataire. Lorsque l’utilisateur sélectionne la case à cocher, MAPI définit cette propriété sur TRUE. Lorsque la case à cocher est désactivée, la propriété est définie sur FALSE.
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md). Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

