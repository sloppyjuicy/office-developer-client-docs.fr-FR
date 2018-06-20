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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784018"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**S’applique à**: Outlook 
  
Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Paramètres

 _lpUid_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section profil à ouvrir. Passage de NULL pour le paramètre _lpUid_ ouvre la section profil de l’appelant. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le mode d’ouverture de la section de profil. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenProfileSection** retournée correctement, éventuellement avant le profil de section est accessible à l’appelant. Si la section profil n’est pas accessible, passer un appel d’objet suivantes permettre provoquer une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler sur l’hypothèse que bénéficie des autorisations en lecture/écriture. 
    
 _lppProfileObj_
  
> [out] Pointeur vers un pointeur vers la section profil ouvert.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La section profil a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour modifier une section de profil en lecture seule ou pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> Il n’est pas une section de profil associée à l’identificateur d’entrée passé _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Indicateurs réservés ou non prises en charge ont été utilisés et, par conséquent, l’opération ne s’est pas terminée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::OpenProfileSection** est implémentée pour tous les objets de prise en charge. Fournisseurs de services et les services de messagerie d’appel **OpenProfileSection** pour ouvrir une section de profil et de récupérer un pointeur vers son implémentation d’interface **IProfSect** . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **OpenProfileSection** ouvre sections profil en lecture seule, sauf si vous définissez l’indicateur ne dans le paramètre _ulFlags_ et votre autorisation est suffisante. Définition de cet indicateur ne garantit pas l’autorisation de lecture/écriture ; les autorisations qui vous sont accordées dépendent de votre niveau d’accès et de l’objet. 
  
Si **OpenProfileSection** tente d’ouvrir une section de profil inexistant en lecture seule, elle renvoie MAPI_E_NOT_FOUND. Si **OpenProfileSection** tente d’ouvrir une section de profil inexistant en lecture-écriture, il crée la section profil et retourne le pointeur **IProfSect** . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

