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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315532"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute une ou plusieurs propriétés de type PT_OBJECT à l'objet.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> dans Pointeur vers un tableau de balises de propriété qui indiquent les propriétés à ajouter.
    
 _lppProblems_
  
> [in, out] Lors de l'entrée, pointeur valide vers une structure [SPropProblemArray](spropproblemarray.md) ou valeur null. En sortie, pointeur vers un pointeur vers une structure qui contient des informations sur les propriétés qui n'ont pas pu être ajoutées, ou NULL. Un pointeur vers une structure de tableau de problèmes de propriété n'est renvoyé qu'en cas de transmission d'un pointeur valide. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement ajoutées.
    
MAPI_E_INVALID_TYPE 
  
> Un type de propriété autre que PT_OBJECT a été transmis dans le tableau vers lequel pointe le paramètre _lpPropTagArray_ . 
    
MAPI_E_NO_ACCESS 
  
> L'objet a été défini pour ne pas autoriser les autorisations en lecture/écriture.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Certaines propriétés ont été ajoutées, mais pas toutes.
    
## <a name="remarks"></a>Remarques

La méthode **IPropData:: HrAddObjProps** ajoute une ou plusieurs propriétés de type PT_OBJECT à l'objet. **HrAddObjProps** fournit une alternative à la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour les propriétés de l'objet, car les propriétés de l'objet ne peuvent pas être créées en appelant **SetProps**. L'ajout d'une propriété d'objet entraîne l'inclusion de la balise de propriété dans la liste des balises de propriété renvoyées par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si **HrAddObjProps** renvoie MAPI_W_PARTIAL_COMPLETION et que vous avez défini _lppProblems_ sur un pointeur valide, vérifiez la structure [SPropProblemArray](spropproblemarray.md) renvoyée pour savoir quelles propriétés n'ont pas été ajoutées. En règle générale, le seul problème qui se produit est le manque de mémoire. Libérez la structure **SPropProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) une fois que vous avez terminé. 
  
Pour ajouter une propriété, l'objet cible doit disposer d'une autorisation en lecture/écriture. Si **HrAddObjProps** renvoie MAPI_E_NO_ACCESS, vous ne pouvez pas ajouter de propriétés à l'objet car il n'autorise pas la modification. Pour obtenir l'autorisation de lecture/écriture sur un objet avant d'appeler **HrAddObjProps**, appelez [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) et définissez le paramètre _ulAccess_ sur IPROP_READWRITE. 
  
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

