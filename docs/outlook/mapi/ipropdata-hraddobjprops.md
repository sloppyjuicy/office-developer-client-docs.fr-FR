---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416383"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriétés qui indiquent les propriétés à ajouter.
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur valide vers une structure [SPropProblemArray](spropproblemarray.md) ou NULL. En sortie, un pointeur vers un pointeur vers une structure qui contient des informations sur les propriétés qui n’ont pas pu être ajoutées, ou NULL. Un pointeur vers une structure de tableau à problème de propriété est renvoyé uniquement si un pointeur valide est passé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été ajoutées avec succès.
    
MAPI_E_INVALID_TYPE 
  
> Un type de propriété autre que PT_OBJECT a été transmis dans le tableau vers qui pointe le paramètre _lpPropTagArray._ 
    
MAPI_E_NO_ACCESS 
  
> L’objet a été définie pour ne pas autoriser l’autorisation de lecture/écriture.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Certaines des propriétés ont été ajoutées, mais pas toutes.
    
## <a name="remarks"></a>Remarques

La **méthode IPropData::HrAddObjProps** ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet. **HrAddObjProps** fournit une alternative à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour les propriétés d’objet, car les propriétés d’objet ne peuvent pas être créées en appelant **SetProps**. L’ajout d’une propriété objet entraîne l’ajout de la balise de propriété dans la liste des balises de propriétés que la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) renvoie. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si **HrAddObjProps** renvoie MAPI_W_PARTIAL_COMPLETION et que vous avez définie  _lppProblems_ sur un pointeur valide, vérifiez la structure [SPropProblemArray](spropproblemarray.md) renvoyée pour connaître les propriétés qui n’ont pas été ajoutées. En règle générale, le seul problème qui se produit est le manque de mémoire. Libérez la structure **SPropProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous en avez terminé. 
  
Pour ajouter une propriété, l’objet cible doit avoir une autorisation de lecture/écriture. Si **HrAddObjProps** renvoie MAPI_E_NO_ACCESS, vous ne pouvez pas ajouter de propriétés à l’objet, car il n’autorise pas la modification. Pour obtenir une autorisation de lecture/écriture sur un objet avant d’appeler **HrAddObjProps,** appelez [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) et définissez le paramètre  _ulAccess_ sur IPROP_READWRITE. 
  
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

