---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783226"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**S’applique à**: Outlook 
  
Décrit un contrôle d’édition qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe :  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>Membres

 **ulbLpszCharsAllowed**
  
> Décalage à partir du début de la structure **DTBLEDIT** pour un filtre de chaîne de caractères qui décrit les restrictions, le cas échéant, pour les caractères qui peuvent être saisis dans le contrôle d’édition. Le filtre n’est pas interprété comme une expression régulière et le même filtre est appliqué à tous les caractères entrés. Le format du filtre est comme suit : 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> |N’importe quel caractère est autorisé (par exemple, `"*"`).  <br/> |
| `[ ]` <br/> |Définit un jeu de caractères (par exemple, `"[0123456789]".`)  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple, `"[a-z]"`).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés (par exemple, `"[~0-9]"`).  <br/> |
| `\` <br/> |Utilisé pour les symboles précédentes quote (par exemple, `"[\-\\\[\]]"` signifie-, \, [, et] caractères sont autorisés).  <br/> |
   
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format du filtre de caractères. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE
  
> Le filtre est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le filtre est au format ANSI.
    
 **ulNumCharsAllowed**
  
> Nombre maximal de caractères que l’utilisateur peut taper dans la zone de texte.
    
 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_TSTRING. Le membre **ulPropTag** identifie la propriété de type chaîne dont les données sont affichées et modifiées dans le contrôle d’édition. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLEDIT** décrit un contrôle d’édition à une zone de la boîte de dialogue qui contient des informations alphanumériques. Presque toutes les boîtes de dialogue ont modifier au moins un contrôle. Les contrôles d’édition peuvent être modifiable par un utilisateur ou en lecture seule. 
  
Les contrôles d’édition peuvent également être la seule ligne ou plusieurs lignes. Contrôles d’édition multilignes ont généralement une barre de défilement associée. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

