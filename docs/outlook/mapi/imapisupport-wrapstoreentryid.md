---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b3850da2917dbf463590643b9e7ba8420f4ea219
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576056"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Convertit un identificateur d’entrée dans le format standard MAPI identificateur d’entrée interne d’une banque de messages.
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> [in] Pointeur vers l’identificateur d’entrée privé pour la banque de messages.
    
 _lpcbWrappedEntry_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée justifiés.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’identificateur d’entrée a été correctement entourée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::WrapStoreEntryID** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services utilisent **WrapStoreEntryID** pour MAPI génère un identificateur d’entrée pour une banque de messages qui encapsule l’identificateur d’entrée interne du magasin. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsqu’un client appelle la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour extraire sa propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) et la banque de messages utilise un identificateur d’entrée dans un format privé, appelez **WrapStoreEntryID **et renvoyer l’identificateur d’entrée indiqué par le paramètre _lppWrappedEntry_ . 
  
Les appels vers les méthodes [IMSProvider::Logon](imsprovider-logon.md) et [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) obtenir toujours un identificateur d’entrée privé du magasin ; la version encapsulée est utilisée uniquement entre les applications clientes et MAPI. 
  
Libérer de la mémoire pour l’identificateur d’entrée indiqué par le paramètre _lppWrappedEntry_ à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous avez terminé, à l’aide de l’identificateur d’entrée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

