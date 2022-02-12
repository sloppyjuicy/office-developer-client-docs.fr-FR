---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: be838ab6d9fbaaef8ece79558bed20fb682dba00
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776514"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie des balises de propriété pour toutes les propriétés. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le format des chaînes dans les balises de propriété renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppPropTagArray_
  
> [out] Pointeur vers un pointeur vers le tableau de balises de propriétés qui contient des balises pour toutes les propriétés de l’objet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Toutes les balises de propriété ont été renvoyées avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIProp::GetPropList** récupère la balise de propriété pour chaque propriété actuellement prise en charge par un objet. Si l’objet ne prend actuellement en charge aucune propriété, **GetPropList** renvoie un tableau de balises de propriétés avec le membre **cValues** définie sur 0. 
  
L’étendue des propriétés renvoyées par **GetPropList** varie d’un fournisseur à l’autre. Certains fournisseurs de services excluent les propriétés pour lesquelles l’appelant n’a pas accès. Tous les fournisseurs retournent des propriétés de type **PT_OBJECT**.
  
Si l’objet ne prend pas en charge Unicode, **GetPropList** renvoie MAPI_E_BAD_CHARWIDTH, même si aucune propriété de chaîne n’est définie pour l’objet. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de transport distant **implémentent GetPropList** exactement comme indiqué ici. Il n’existe aucune préoccupation particulière. Votre implémentation doit, bien entendu, renvoyer la même liste de propriétés que prise en charge par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez la [fonction MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de balises de propriétés pointé par  _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetPropList** pour obtenir une liste de propriétés à transmettre à **GetProps**. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

