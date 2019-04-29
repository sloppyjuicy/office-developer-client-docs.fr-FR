---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411385"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une section du profil actif et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Paramètres

 _lpUid_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil à ouvrir. Le fait de transmettre NULL pour le paramètre _lpUid_ ouvre la section profil de l'appelant. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'ouverture de la section profil. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement accessible à l'appelant. Si la section profil n'est pas accessible, un appel d'objet ultérieur peut entraîner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
 _lppProfileObj_
  
> remarquer Pointeur vers un pointeur vers la section de profil ouverte.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d'une section de profil en lecture seule ou d'accès à un objet pour lequel l'appelant ne dispose pas des autorisations suffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> Il n'existe pas de section de profil associée à l'identificateur d'entrée passé dans _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Des indicateurs réservés ou non pris en charge ont été utilisés et, par conséquent, l'opération ne s'est pas terminée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: OpenProfileSection** est implémentée pour tous les objets de prise en charge. Services de messagerie et fournisseurs d'appels **OpenProfileSection** pour ouvrir une section de profil et récupérer un pointeur vers son implémentation d'interface **IProfSect** . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **OpenProfileSection** ouvre les sections de profil en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY dans le paramètre _ulFlags_ et que votre autorisation est suffisante. La définition de cet indicateur ne garantit pas l'autorisation en lecture/écriture; les autorisations que vous avez accordées dépendent de votre niveau d'accès et de l'objet. 
  
Si **OpenProfileSection** tente d'ouvrir une section de profil inexistante en lecture seule, elle renvoie MAPI_E_NOT_FOUND. Si **OpenProfileSection** tente d'ouvrir une section de profil qui n'existe pas en lecture/écriture, il crée la section profile et renvoie le pointeur **IProfSect** . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

