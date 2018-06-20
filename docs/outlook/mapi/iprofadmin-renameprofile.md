---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784379"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**S’applique à**: Outlook 
  
Affecte un nouveau nom à un profil.
  
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode. 
    
 _ulFlags_
  
> [in] Toujours NULL.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le profil a été renommé.
    
MAPI_E_LOGON_FAILED 
  
> Le mot de passe de profil est incorrecte.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::RenameProfile** attribue un nouveau nom à un profil, le cas échéant. Si le profil pour renommer est en cours d’utilisation par un client lorsque **RenameProfile** est appelée, **RenameProfile** marque le profil et renvoie S_OK au lieu d’essayer de l’opération de changement alors que le profil est en cours d’utilisation. Lorsque le profil est n’est plus utilisé, **RenameProfile** assigne le nouveau nom. 
  
Les noms anciens et nouveaux du profil peuvent contenir jusqu'à 64 caractères et peuvent inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement.
    
- Des espaces, mais pas espaces à gauche ou.
    
Le _lpszPassword_ doit toujours être NULL ou un pointeur vers une chaîne de longueur nulle. 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

