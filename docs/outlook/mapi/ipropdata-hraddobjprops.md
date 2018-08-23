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
ms.openlocfilehash: ae0d6d58f96738a9686dbdda86336c040c2e2f68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591681"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Param�tres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriété qui indiquent les propriétés à ajouter.
    
 _lppProblems_
  
> [entrée, sortie] Sur entrée, un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) valide ou valeur NULL. Dans la sortie, un pointeur vers un pointeur vers une structure qui contient des informations sur les propriétés qui ne peut pas être ajouté ou NULL. Un pointeur vers une structure de tableau de problème de propriété est renvoyé uniquement si un pointeur valide est passé. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les propriétés ont été ajoutées.
    
MAPI_E_INVALID_TYPE 
  
> Une propriété de type autre que PT_OBJECT a été passée dans le paramètre _lpPropTagArray_ pointe vers le tableau. 
    
MAPI_E_NO_ACCESS 
  
> L’objet a été défini ne pas pour accorder l’autorisation de lecture/écriture.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> Certains, mais pas toutes les propriétés ont été ajoutés.
    
## <a name="remarks"></a>Remarques

La méthode **IPropData::HrAddObjProps** ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet. **HrAddObjProps** propose une alternative à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour les propriétés de l’objet, car les propriétés de l’objet ne peut pas être créées en appelant **SetProps**. Ajout d’un objet entraîne de propriété dans la balise de propriété soient incluse dans la liste des balises de propriété retournée par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si **HrAddObjProps** renvoie MAPI_W_PARTIAL_COMPLETION se produit et que vous avez défini un pointeur valide _lppProblems_ , vérifiez la structure [SPropProblemArray](spropproblemarray.md) retournée permettant de savoir quelles propriétés n’ont pas été ajoutées. En règle générale, le seul problème qui se produit est manque de mémoire. Libérer la structure **SPropProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous avez terminé avec lui. 
  
Pour ajouter une propriété, l’objet de cible doit avoir des autorisations en lecture-écriture. Si **HrAddObjProps** renvoie MAPI_E_NO_ACCESS, vous ne pouvez pas ajouter des propriétés à l’objet car il ne permet pas de modification. Pour obtenir l’autorisation de lecture/écriture à un objet avant d’appeler **HrAddObjProps**, appelez [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) et définissez le paramètre _ulAccess_ IPROP_READWRITE. 
  
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

