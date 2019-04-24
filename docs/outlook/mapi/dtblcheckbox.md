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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287268"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur une case à cocher qui sera utilisée dans une boîte de dialogue construite à partir d'une table d'affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
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
  
> Position en mémoire de la chaîne de caractères qui s'affiche avec la case à cocher. 
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format de l'étiquette de case à cocher. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> L'étiquette est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.
    
 **ulPRPropertyName**
  
> Balise de propriété pour une propriété de type PT_BOOLEAN. La valeur de cette propriété est affectée par l'état de la case à cocher.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLCHECKBOX** décrit une case à cocher qui reflète l'un des deux États suivants: activé (case cochée) ou désactivé (zone vide). 
  
Le membre **ulPRPropertyName** décrit une propriété booléenne dont la valeur est manipulée en modifiant l'état de la case à cocher. Lorsque la case à cocher est affichée pour la première fois, MAPI appelle la méthode **GetProps** de l'implémentation **IMAPIProp** associée à la table d'affichage pour récupérer un jeu de propriétés par défaut. Si l'une des propriétés est mappée à la balise de propriété dans la structure **DTBLCHECKBOX** , la valeur de cette propriété est affichée en tant que valeur initiale de la case à cocher. 
  
Les contrôles de case à coCher peuvent être modifiables. Cela permet à un utilisateur de modifier son état. Les cases à cocher modifiables définissent l'indicateur DT_EDITABLE dans le membre **ulCtlFlags** de leur structure [DTCTL](dtctl.md) et dans leur propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Lorsqu'une case à cocher modifie son état, MAPI appelle [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir la propriété identifiée dans le membre de la balise de propriété de la structure **DTBLCHECKBOX** sur le nouvel État. 
  
Par exemple, un fournisseur de carnet d'adresses peut inclure un contrôle de case à cocher modifiable dans sa boîte de dialogue de configuration pour ajuster le paramètre de la propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) d'un destinataire. Lorsque l'utilisateur active la case à cocher, MAPI affecte à cette propriété la valeur TRUE. Lorsque la case à cocher est désactivée, la propriété est définie sur FALSe.
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md). Pour plus d'informations sur les types de propriétés, voir [MAPI Property type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

