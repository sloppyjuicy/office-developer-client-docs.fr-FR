---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571121"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les balises de propriété pour toutes les propriétés. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le format des chaînes dans les balises de propriété renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppPropTagArray_
  
> [out] Pointeur vers un pointeur vers le tableau de balise de propriété qui contient des balises pour toutes les propriétés de l’objet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Toutes les balises de propriété ont été renvoyées.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetPropList** récupère la balise de propriété pour chaque propriété actuellement pris en charge par un objet. Si l’objet ne prend pas en charge toutes les propriétés, **GetPropList** renvoie un tableau de balise de propriété avec le membre **cValues** défini sur 0. 
  
La portée des propriétés retournées par **GetPropList** varie d’un fournisseur. Certains fournisseurs de services excluent les propriétés pour lesquelles l’appelant n’a pas accès. Tous les fournisseurs de renvoient les propriétés de type **PT_OBJECT**.
  
Si l’objet ne prend pas en charge Unicode, **GetPropList** renvoie MAPI_E_BAD_CHARWIDTH, même si aucune propriété de chaîne définis pour l’objet. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Fournisseurs de transport à distance implémentent **GetPropList** exactement comme indiqué ici. Il n’existe aucune problèmes spéciaux. Votre implémentation doit retourner bien sûr, la même liste des propriétés de prise en charge par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de balise de propriété désigné par _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetPropList** pour obtenir une liste de propriétés à transmettre à **GetProps**.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

