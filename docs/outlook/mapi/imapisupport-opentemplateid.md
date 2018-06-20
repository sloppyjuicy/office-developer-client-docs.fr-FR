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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784031"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**S’applique à**: Outlook 
  
Ouvre une entrée de destinataires dans un fournisseur de carnet d’adresse étrangère.
  
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
  
> [in] Le nombre d’octets dans l’identificateur de modèle désigné par _lpTemplateID_. 
    
 _lpTemplateID_
  
> [in] Pointeur vers l’identificateur du modèle propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de l’entrée de destinataire à ouvrir.
    
 _ulTemplateFlags_
  
> [in] Un masque binaire composé des indicateurs utilisés pour décrire comment ouvrir l’entrée. Vous pouvez définir l’indicateur suivant :
    
FILL_ENTRY 
  
> Une nouvelle entrée est créée. Lorsque le fournisseur étranger reçoit le prochain appel [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) MAPI, il peut contrôler la création de l’entrée en modifiant les propriétés indiquées par le paramètre _lpMAPIPropData_ ou en retournant une interface spécifique mise en œuvre dans _lppMAPIPropNew_ pour contrôler la définition des propriétés de la nouvelle entrée. 
    
 _lpMAPIPropData_
  
> [in] Pointeur vers l’implémentation d’interface de l’appelant à accéder à l’entrée. Il s’agit de l’implémentation du fournisseur étranger pouvant envelopper avec sa propre implémentation et retourner dans le paramètre _lppMAPIPropNew_ . Le paramètre _lpMAPIPropData_ doit pointer sur une implémentation d’interface en lecture/écriture qui dérive de [IMAPIProp : IUnknown](imapipropiunknown.md) et prend en charge l’interface demandée dans le paramètre _lpInterface_ . 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’entrée. Le paramètre _lppMAPIPropNew_ pointe vers une interface du type spécifié par _lpInterface_. Passage de NULL renvoie l’interface standard pour un utilisateur de messagerie, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Pointeur vers l’implémentation d’interface que le fournisseur étranger donne pour accéder à l’entrée.
    
 _lpMAPIPropSibling_
  
> Réservé ; doit être NULL.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le processus de liaison a réussi.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le fournisseur de carnet d’adresse étrangère n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::OpenTemplateID** est implémentée uniquement pour les objets de prise en charge du fournisseur adresse téléchargeable. **OpenTemplateID** est appelé uniquement par les fournisseurs de carnet d’adresses qui peuvent agir en tant qu’hôtes pour les entrées qui appartiennent à d’autres fournisseurs de carnet d’adresses, également appelé étrangères fournisseurs. Fournisseurs d’hébergement appellent **OpenTemplateID** pour ouvrir une entrée étrangère, ce qui se produit lorsque des données dans le fournisseur d’hébergement sont liées au code dans le fournisseur étranger. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez **OpenTemplateID** uniquement si vous prenez en charge le stockage des entrées avec les identificateurs de modèle à partir des fournisseurs de carnet d’adresse étrangère. Cette prise en charge impose des exigences supplémentaires sur vos implémentations [IABContainer::CreateEntry](iabcontainer-createentry.md) et [IABLogon::OpenEntry](iablogon-openentry.md) . Pour plus d’informations, consultez les descriptions de ces méthodes [agissant comme un fournisseur de carnet d’adresses hôte](acting-as-a-host-address-book-provider.md).
  
Si l’appel **OpenTemplateID** renvoie l’interface liée l’implémentation d’objet même propriété que vous avez passé, vous pouvez libérer la référence à votre objet de la propriété. Il s’agit, car le fournisseur étranger a appelé la méthode l’objet **AddRef** pour garder sa propre référence. Si le fournisseur étranger n’a pas besoin de conserver une référence à l’objet property, **OpenTemplateID** renvoie l’objet property indépendant. 
  
En cas d’échec de **OpenTemplateID** avec MAPI_E_UNKNOWN_ENTRYID, essayez de continuer à traiter l’entrée en lecture seule. 
  
## <a name="see-also"></a>Voir aussi



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Propriété canonique PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

