---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418504"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une entrée de destinataire dans un fournisseur de carnet d’adresses étranger.
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parameters

 _cbTemplateID_
  
> [in] Nombre d’byte dans l’identificateur de modèle pointé par  _lpTemplateID_. 
    
 _lpTemplateID_
  
> [in] Pointeur vers l’identificateur **de modèle PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de l’entrée du destinataire à ouvrir.
    
 _ulTemplateFlags_
  
> [in] Masque de bits d’indicateurs utilisé pour décrire comment ouvrir l’entrée. L’indicateur suivant peut être définie :
    
FILL_ENTRY 
  
> Une nouvelle entrée est créée. Lorsque le fournisseur étranger reçoit l’appel [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) suivant de MAPI, il peut contrôler la façon dont l’entrée est créée en modifiant les propriétés pointées par le paramètre  _lpMAPIPropData_ ou en renvoyant une implémentation d’interface spécifique dans  _lppMAPIPropNew_ pour contrôler la façon dont les propriétés de la nouvelle entrée sont définies. 
    
 _lpMAPIPropData_
  
> [in] Pointeur vers l’implémentation de l’interface que l’appelant utilise pour accéder à l’entrée. Il s’agit de l’implémentation que le fournisseur étranger peut encapsuler avec sa propre implémentation et retourner dans le paramètre _lppMAPIPropNew._ Le paramètre _lpMAPIPropData_ doit pointer vers une implémentation d’interface en lecture/écriture qui dérive [d’IMAPIProp : IUnknown](imapipropiunknown.md) et prend en charge l’interface demandée dans le paramètre _lpInterface._ 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’entrée. Le  _paramètre lppMAPIPropNew_ pointe vers une interface du type spécifié par  _lpInterface_. La transmission null renvoie l’interface standard d’un utilisateur de messagerie, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Pointeur vers l’implémentation de l’interface que le fournisseur étranger fournit pour accéder à l’entrée.
    
 _lpMAPIPropSibling_
  
> Réservé ; doit être NULL.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de liaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnet d’adresses étranger n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::OpenTemplateID** est implémentée uniquement pour les objets de prise en charge du fournisseur de carnet d’adresses. **OpenTemplateID** est appelé uniquement par les fournisseurs de carnet d’adresses qui peuvent agir en tant qu’hôtes pour les entrées appartenant à d’autres fournisseurs de carnet d’adresses, également appelés fournisseurs étrangers. Les fournisseurs d’hôtes **appellent OpenTemplateID** pour ouvrir une entrée étrangère, ce qui se produit lorsque les données du fournisseur hôte sont liées au code dans le fournisseur étranger. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **OpenTemplateID uniquement** si vous appelez le stockage d’entrées avec des identificateurs de modèles provenant de fournisseurs de carnets d’adresses étrangers. Cette prise en charge place des exigences supplémentaires sur vos [implémentations IABContainer::CreateEntry](iabcontainer-createentry.md) et [IABLogon::OpenEntry.](iablogon-openentry.md) Pour plus d’informations, voir les descriptions de ces méthodes et agir en tant que fournisseur de [carnet d’adresses hôte.](acting-as-a-host-address-book-provider.md)
  
Si **l’appel OpenTemplateID** renvoie en tant qu’interface liée la même implémentation d’objet de propriété que celle que vous avez passée, vous pouvez libérer votre référence à votre objet de propriété. Cela est dû au fait que le fournisseur étranger a appelé la méthode **AddRef** de l’objet pour conserver sa propre référence. Si le fournisseur étranger n’a pas besoin de conserver une référence à l’objet de propriété, **OpenTemplateID** retourne l’objet de propriété indépendant. 
  
Si **OpenTemplateID** échoue avec MAPI_E_UNKNOWN_ENTRYID, essayez de continuer en traitant l’entrée comme étant en lecture seule. 
  
## <a name="see-also"></a>Voir aussi



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Propriété canonique PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

