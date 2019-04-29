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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414787"
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

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le format des chaînes dans les balises de propriété renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lppPropTagArray_
  
> remarquer Pointeur vers un pointeur vers le tableau de balises de propriété qui contient des balises pour toutes les propriétés de l'objet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Toutes les balises de propriété ont été renvoyées avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp:: GetPropList** extrait la balise de propriété pour chaque propriété actuellement prise en charge par un objet. Si l'objet ne prend actuellement en charge aucune propriété, **GetPropList** renvoie un tableau de balises de propriété avec le membre **cValues** défini sur 0. 
  
L'étendue des propriétés retournées par **GetPropList** varie en fonction du fournisseur et du fournisseur. Certains fournisseurs de services excluent les propriétés pour lesquelles l'appelant n'a pas accès. Tous les fournisseurs renvoient les propriétés de type **PT_OBJECT**.
  
Si l'objet ne prend pas en charge le format Unicode, **GetPropList** renvoie MAPI_E_BAD_CHARWIDTH, même s'il n'existe aucune propriété de chaîne définie pour l'objet. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de transport à distance implémentent **GetPropList** exactement comme spécifié ici. Il n'y a aucune préoccupation particulière. Votre implémentation doit, bien sûr, renvoyer la même liste de propriétés que celle prise en charge par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de balises de propriété pointé par _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp:: GetPropList** pour obtenir une liste de propriétés à transmettre à **GetProps**.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

