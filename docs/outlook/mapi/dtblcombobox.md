---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406975"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle de zone de liste déroulante qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Décalage entre le début de la structure **DTBLCOMBOBOX** et un filtre de chaîne de caractères qui décrit les restrictions, le casque, et les caractères qui peuvent être entrés dans le contrôle d’édition de la zone de liste déroulante. Le filtre n’est pas interprété comme une expression régulière et le même filtre est appliqué à chaque caractère entré. Le format du filtre est le suivant : 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> |Tout caractère est autorisé (par exemple,  `"*"` ).  <br/> |
| `[ ]` <br/> |Définit un ensemble de caractères (par exemple,  `"[0123456789]"` ).  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple,  `"[a-z]"` ).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés. (par exemple,  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Utilisé pour guillemets l’un des symboles précédents (par exemple, les caractères  `"[\-\\\[\]]"` -, \, [et ] sont autorisés).  <br/> |
   
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format du filtre de chaîne de caractères. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Le filtre est au format Unicode. Si l MAPI_UNICODE n’est pas définie, le filtre est au format ANSI.
    
 **ulNumCharsAllowed**
  
> Nombre maximal de caractères qui peuvent être entrés dans la zone de texte de la zone de liste déroulante.
    
 **ulPRPropertyName**
  
> Balise de propriété pour une propriété de type PT_TSTRING. 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de type PT_OBJECT sur laquelle une interface **IMAPITable** peut être ouverte à l’aide d’un **appel OpenProperty.** La table doit avoir une colonne avec une propriété du même type que la propriété identifiée par le membre **ulPRPropertyName.** Les lignes du tableau sont utilisées pour remplir la liste. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLCOMBOBOX** décrit une zone de liste déroulante composée d’une liste et d’un champ de sélection. La liste présente les informations à partir des lesquelles un utilisateur peut sélectionner, et le champ de sélection affiche la sélection actuelle. Le champ de sélection est un contrôle d’édition qui peut également être utilisé pour entrer du texte qui n’est pas déjà dans la liste. 
  
Les deux membres de balise de propriété fonctionnent ensemble pour coordonner l’affichage de liste avec le contrôle d’édition. Lorsque MAPI affiche la zone de liste déroulante pour la première fois, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** associée à la table d’affichage pour récupérer la table représentée par le membre **ulPRTableName.** Cette table contient une colonne contenant les valeurs de la propriété représentée par le membre **ulPRPropertyName.** Par conséquent, cette colonne doit être du même type que la propriété **ulPRPropertyName** et les deux colonnes doivent être des chaînes de caractères. 
  
Les valeurs de la colonne sont affichées dans la section de liste de la zone de liste déroulante. Par conséquent, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) n’est pas une balise de propriété valide pour **ulPRPropertyName**. Lorsqu’un utilisateur sélectionne l’une des lignes ou entre de nouvelles données dans la zone de texte, la propriété **ulPRPropertyName** est définie sur la valeur sélectionnée ou entrée. 
  
Pour afficher une valeur initiale pour le contrôle d’édition, MAPI appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer les valeurs de propriété du tableau d’affichage. Si l’une des propriétés récupérées correspond à la propriété représentée par le membre **ulPRPropertyName,** sa valeur devient la valeur initiale. 
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

