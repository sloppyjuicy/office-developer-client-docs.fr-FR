---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
ms.openlocfilehash: 4005497ad0e3b5285f5363f0f26c17c85df7208b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370231"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Attribue un nouveau nom à un profil.
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszOldProfileName_
  
> [in] Pointeur vers le nom actuel du profil à renommer.
    
 _lpszOldPassword_
  
> [in] Toujours NULL.
    
 _lpszNewProfileName_
  
> [in] Pointeur vers le nouveau nom du profil à renommer.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. 
    
 _ulFlags_
  
> [in] Toujours NULL.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le profil a été renommé avec succès.
    
MAPI_E_LOGON_FAILED 
  
> Le mot de passe du profil est incorrect.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le **bouton Annuler dans** une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::RenameProfile** attribue un nouveau nom à un profil, s’il en possède un. Si le profil à renommer est utilisé par un client lorsque **RenameProfile** est appelé, **RenameProfile** marque le profil et renvoie S_OK au lieu de tenter l’opération de changement de nom pendant l’utilisation du profil. Lorsque le profil n’est plus utilisé, **RenameProfile** lui attribue le nouveau nom. 
  
L’ancien et le nouveau nom du profil peuvent comporter jusqu’à 64 caractères et inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuateur et le caractère de soulignement.
    
- Espaces incorporés, mais pas espaces de début ou de fin.
    
_LpszPassword doit_ toujours être NULL ou pointeur vers une chaîne de longueur nulle. 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

