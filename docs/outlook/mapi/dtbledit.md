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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404679"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle d'édition qui sera utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
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
  
> Offset entre le début de la structure **DTBLEDIT** et un filtre de chaîne de caractères qui décrit les restrictions, le cas échéant, des caractères pouvant être entrés dans le contrôle d'édition. Le filtre n'est pas interprété comme une expression régulière et le même filtre est appliqué à tous les caractères entrés. Le format du filtre est le suivant: 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> |N'importe quel caractère est autorisé (par `"*"`exemple,).  <br/> |
| `[ ]` <br/> |Définit un jeu de caractères (par exemple, `"[0123456789]".`)  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple, `"[a-z]"`).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés (par exemple `"[~0-9]"`,).  <br/> |
| `\` <br/> |Utilisé pour citer tous les symboles précédents (par exemple, `"[\-\\\[\]]"` les caractères «, \, » et «») sont autorisés.  <br/> |
   
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format du filtre de caractères. L'indicateur suivant peut être défini:
    
MAPI_UNICODE
  
> Le filtre est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le filtre est au format ANSI.
    
 **ulNumCharsAllowed**
  
> Nombre maximal de caractères que l'utilisateur peut entrer dans la zone de texte.
    
 **ulPropTag**
  
> Balise de propriété pour une propriété de type PT_TSTRING. Le membre **ulPropTag** identifie la propriété de chaîne dont les données sont affichées et modifiées dans le contrôle d'édition. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLEDIT** décrit un contrôle d'édition d'une zone dans une boîte de dialogue qui contient des informations alphanumériques. Presque toutes les boîtes de dialogue possèdent au moins un contrôle d'édition. Les contrôles d'édition peuvent être modifiables par un utilisateur ou en lecture seule. 
  
Les contrôles d'édition peuvent également être à ligne unique ou multiligne. Les contrôles d'édition multiligne ont généralement une barre de défilement associée. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

