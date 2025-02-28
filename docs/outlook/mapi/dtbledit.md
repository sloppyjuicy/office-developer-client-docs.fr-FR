---
title: DTBLEDIT
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: Décrit un contrôle d’édition qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.
ms.openlocfilehash: a685b1befde345f9aaae7b4d5f91b612e2d65a18
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781788"
---
# <a name="dtbledi"></a>DTBLEDI
  
**S’applique à** : Outlook 2013 | Outlook 2016
  
Décrit un contrôle d’édition qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.

|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête : |Mapidefs.h |
|Macro associée : |[SizedDtblEdit](sizeddtbledit.md) |

```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Décalage entre le début de la structure **DTBLEDIT** et un filtre de chaîne de caractères qui décrit les restrictions, le casque, et les caractères qui peuvent être entrés dans le contrôle d’édition. Le filtre n’est pas interprété comme une expression régulière et le même filtre est appliqué à chaque caractère entré. Le format du filtre est le suivant :

|**Caractère**|**Description**|
|:-----|:-----|
| `*`   |Tout caractère est autorisé (par exemple, `"*"`). |
| `[ ]` |Définit un ensemble de caractères (par exemple, `"[0123456789]".`) |
| `-`   |Indique une plage de caractères (par exemple, `"[a-z]"`). |
| `~`   |Indique que ces caractères ne sont pas autorisés (par exemple, `"[~0-9]"`). |
| `\`   |Utilisé pour guillemets l’un des symboles précédents (par exemple, `"[\-\\\[\]]"` les caractères -, \, [et ] sont autorisés). |

 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format du filtre de caractères. L’indicateur suivant peut être définie :

MAPI_UNICODE
  
> Le filtre est au format Unicode. Si l MAPI_UNICODE n’est pas définie, le filtre est au format ANSI.

 **ulNumCharsAllowed**
  
> Nombre maximal de caractères que l’utilisateur peut taper dans la zone de texte.

 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_TSTRING. Le **membre ulPropTag** identifie la propriété de chaîne dont les données sont affichées et modifiées dans le contrôle d’édition.

## <a name="remarks"></a>Remarques

Une structure **DTBLEDIT décrit** un contrôle d’édition d’une zone dans une boîte de dialogue qui contient des informations alphanumériques. Presque toutes les boîtes de dialogue ont au moins un contrôle d’édition. Les contrôles d’édition peuvent être modifiables par un utilisateur ou en lecture seule.
  
Les contrôles d’édition peuvent également être à une seule ligne ou à plusieurs lignes. Les contrôles d’édition multiligne sont généralement associés à une barre de défilement.
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi

[DTCTL](dtctl.md)  
[IMAPIProp::GetProps](imapiprop-getprops.md)  
Propriété canonique [PidTagControlType](pidtagcontroltype-canonical-property.md)
 [Structures MAPI](mapi-structures.md)
