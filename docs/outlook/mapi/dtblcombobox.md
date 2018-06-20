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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783215"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**S’applique à**: Outlook 
  
Décrit un contrôle de zone de liste déroulante qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe :  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a>Membres

 **ulbLpszCharsAllowed**
  
> Décalage à partir du début de la structure **DTBLCOMBOBOX** pour un filtre de chaîne de caractères qui décrit les restrictions, si le contrôle d’édition aux caractères qui peuvent être saisis dans la zone de liste modifiable. Le filtre n’est pas interprété comme une expression régulière et le même filtre est appliqué à tous les caractères entrés. Le format du filtre est comme suit : 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> |N’importe quel caractère est autorisé (par exemple, `"*"`).  <br/> |
| `[ ]` <br/> |Définit un jeu de caractères (par exemple, `"[0123456789]"`).  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple, `"[a-z]"`).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés. (par exemple, `"[~0-9]"`).  <br/> |
| `\` <br/> |Utilisé pour les symboles précédentes quote (par exemple, `"[\-\\\[\]]"` signifie-, \, [, et] caractères sont autorisés).  <br/> |
   
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format du filtre chaîne de caractères. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Le filtre est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le filtre est au format ANSI.
    
 **ulNumCharsAllowed**
  
> Nombre maximal de caractères qui peuvent être entrées dans la zone de texte de la zone de liste modifiable.
    
 **ulPRPropertyName**
  
> Balise de propriété pour une propriété de type PT_TSTRING. 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de type PT_OBJECT sur lequel une interface **IMAPITable** peut être ouvert à l’aide d’un appel **OpenProperty** . Le tableau doit avoir une colonne avec une propriété qui est du même type que la propriété identifiée par le membre **ulPRPropertyName** . Les lignes du tableau sont utilisés pour remplir la liste. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLCOMBOBOX** décrit un contrôle qui se compose d’une liste et un champ de sélection de zone de liste modifiable. La liste présente les informations à partir de laquelle un utilisateur peut sélectionner, et le champ de sélection affiche la sélection actuelle. Le champ de sélection est un contrôle d’édition qui peut également servir à entrer du texte pas déjà dans la liste. 
  
Les membres de balise de deux propriété travaillent ensemble pour coordonner l’affichage de liste avec le contrôle d’édition. Lorsque MAPI affiche la zone de liste déroulante, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** qui est associée à la table d’affichage pour extraire la table représentée par le membre **ulPRTableName** . Cette table a une colonne à une colonne qui contient des valeurs pour la propriété représentée par le membre **ulPRPropertyName** . Par conséquent, cette colonne doit être du même type que la propriété **ulPRPropertyName** et les deux colonnes doivent être des chaînes de caractères. 
  
Les valeurs de la colonne sont affichées dans la section liste de la zone de liste déroulante. Par conséquent, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) n’est pas une balise de propriété valide pour **ulPRPropertyName**. Lorsqu’un utilisateur sélectionne l’une des lignes ou entre les nouvelles données dans la zone de texte, la propriété **ulPRPropertyName** est définie à la valeur entrée ou sélectionnée. 
  
Pour afficher une valeur initiale pour le contrôle d’édition, MAPI appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer les valeurs de propriété de l’affichage du tableau. Si une des propriétés récupérées correspond à la propriété représentée par le membre **ulPRPropertyName** , sa valeur est la valeur initiale. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[Propriété canonique PidTagControlType](pidtagcontroltype-canonical-property.md)


[Structures MAPI](mapi-structures.md)

