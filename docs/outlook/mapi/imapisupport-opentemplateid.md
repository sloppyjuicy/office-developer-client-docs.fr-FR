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
  
Ouvre une entrée de destinataire dans un fournisseur de carnets d'adresses étrangers.
  
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

## <a name="parameters"></a>Paramètres

 _cbTemplateID_
  
> dans Nombre d'octets dans l'identificateur de modèle pointé par _lpTemplateID_. 
    
 _lpTemplateID_
  
> dans Pointeur vers la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de l'identificateur de modèle de l'entrée de destinataire à ouvrir.
    
 _ulTemplateFlags_
  
> dans Masque de des indicateurs utilisés pour décrire l'ouverture de l'entrée. L'indicateur suivant peut être défini:
    
FILL_ENTRY 
  
> Une nouvelle entrée est créée. Lorsque le fournisseur étranger reçoit l'appel [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) à partir de MAPI, il peut contrôler la manière dont l'entrée est créée en modifiant les propriétés pointées par le paramètre _lpMAPIPropData_ ou en renvoyant une interface spécifique. implémentation dans _lppMAPIPropNew_ pour contrôler la définition des propriétés de la nouvelle entrée. 
    
 _lpMAPIPropData_
  
> dans Pointeur vers l'implémentation de l'interface que l'appelant utilise pour accéder à l'entrée. Il s'agit de l'implémentation que le fournisseur étranger peut encapsuler avec sa propre implémentation et renvoyer le paramètre _lppMAPIPropNew_ . Le paramètre _lpMAPIPropData_ doit pointer vers une implémentation d'interface en lecture/écriture qui dérive de [IMAPIProp: IUnknown](imapipropiunknown.md) et prend en charge l'interface demandée dans le paramètre _lpInterface_ . 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'entrée. Le paramètre _lppMAPIPropNew_ pointe vers une interface du type spécifié par _lpInterface_. Le passage de NULL renvoie l'interface standard pour un utilisateur de messagerie, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> remarquer Pointeur vers l'implémentation de l'interface que le fournisseur étranger fournit pour accéder à l'entrée.
    
 _lpMAPIPropSibling_
  
> MSR doit être NULL.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de liaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnets d'adresses étrangers n'existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: OpenTemplateID** est implémentée uniquement pour les objets de prise en charge du fournisseur de carnet d'adresses. **OpenTemplateID** est appelé uniquement par les fournisseurs de carnet d'adresses qui peuvent agir comme des hôtes pour les entrées appartenant à d'autres fournisseurs de carnet d'adresses, également appelés fournisseurs étrangers. Les fournisseurs d'hôtes appellent **OpenTemplateID** pour ouvrir une entrée étrangère, qui se produit lorsque les données du fournisseur hôte sont liées au code dans le fournisseur étranger. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **OpenTemplateID** uniquement si vous prenez en charge le stockage des entrées avec des identificateurs de modèle provenant de fournisseurs de carnet d'adresses étrangers. Cette prise en charge impose des exigences supplémentaires sur vos implémentations de [IABContainer:: CreateEntry](iabcontainer-createentry.md) et [IABLogon:: OpenEntry](iablogon-openentry.md) . Pour plus d'informations, consultez les descriptions de ces méthodes et [agir en tant que fournisseur de carnets d'adresses hôte](acting-as-a-host-address-book-provider.md).
  
Si l'appel **OpenTemplateID** est renvoyé en tant qu'interface liée à la même implémentation d'objet de propriété que celle que vous avez passée, vous pouvez libérer votre référence à votre objet Property. Cela est dû au fait que le fournisseur étranger a appelé la méthode **AddRef** de l'objet pour conserver sa propre référence. Si le fournisseur étranger n'a pas besoin de conserver une référence à l'objet Property, **OpenTemplateID** renverra l'objet de propriété indépendant. 
  
Si **OpenTemplateID** échoue avec MAPI_E_UNKNOWN_ENTRYID, essayez de continuer en traitant l'entrée comme étant en lecture seule. 
  
## <a name="see-also"></a>Voir aussi



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Propriété canonique PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

