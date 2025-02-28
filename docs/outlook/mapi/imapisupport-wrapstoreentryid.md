---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
ms.openlocfilehash: 1ca9df5ac30ab1926fd818eadc9d024d0f4fdca2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381529"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit l’identificateur d’entrée interne d’une boutique de messages en identificateur d’entrée au format mapi standard.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Paramètres

 _cbOrigEntry_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> [in] Pointeur vers l’identificateur d’entrée privée de la banque de messages.
    
 _lpcbWrappedEntry_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par  _le paramètre lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée wrapped.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée a été correctement wrapped.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::WrapStoreEntryID** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services **utilisent WrapStoreEntryID** pour que MAPI génère un identificateur d’entrée pour une magasin de messages qui encapsule l’identificateur d’entrée interne de la boutique. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsqu’un client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de votre banque de messages pour récupérer sa propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) et que votre banque de messages utilise un identificateur d’entrée dans un format privé, appelez **WrapStoreEntryID** et renvoyez l’identificateur d’entrée pointé par le paramètre  _lppWrappedEntry_ . 
  
Les appels aux méthodes [IMSProvider::Logon](imsprovider-logon.md) et [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) obtiennent toujours l’identificateur d’entrée privée du magasin ; La version wrapped est utilisée uniquement entre les applications clientes et MAPI. 
  
Libérez la mémoire de l’identificateur d’entrée pointé par le paramètre  _lppWrappedEntry_ à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous avez terminé d’utiliser l’identificateur d’entrée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

