---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309568"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie un profil.
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszOldProfileName_
  
> dans Pointeur vers le nom du profil à copier.
    
 _lpszOldPassword_
  
> dans Pointeur vers le mot de passe du profil à copier.
    
 _lpszNewProfileName_
  
> dans Pointeur vers le nouveau nom du profil copié.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le profil est copié. Les indicateurs suivants peuvent être définis:
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue qui invite l'utilisateur à indiquer le mot de passe correct du profil à copier. Si cet indicateur n'est pas défini, aucune boîte de dialogue ne s'affiche.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le profil a été correctement copié.
    
MAPI_E_ACCESS_DENIED 
  
> Le nouveau nom de profil est identique à celui d'un profil existant.
    
MAPI_E_LOGON_FAILED 
  
> Le mot de passe du profil à copier est incorrect et une boîte de dialogue n'a pas pu être affichée à l'utilisateur pour demander le mot de passe correct car MAPI_DIALOG n'a pas été défini dans le paramètre _ulFlags_ . 
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n'existe pas.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin:: CopyProfile** effectue une copie du profil désigné par _lpszOldProfileName_, lui donnant le nom indiqué par _lpszNewProfileName_. La copie d'un profil laisse la copie avec le même mot de passe que l'original.
  
Le nom du profil d'origine, son mot de passe et la copie peuvent contenir jusqu'à 64 caractères et peuvent inclure les caractères suivants:
  
- Tous les caractères alphanumériques, y compris les caractères d'accentuation et le trait de soulignement.
    
- Espaces incorporés, mais pas d'espaces de début ou de fin.
    
Les mots de passe de profil ne sont pas pris en charge sur tous les systèmes d'exploitation. Sur les systèmes d'exploitation qui ne prennent pas en charge les mots de passe de profil, _lpszOldPassword_ peut être null ou un pointeur vers une chaîne de longueur nulle. 
  
Si _lpszOldPassword_ est défini sur null, le profil à copier requiert un mot de passe et l'indicateur MAPI_DIALOG est défini; une boîte de dialogue invitant l'utilisateur à indiquer le mot de passe est affichée. Si un mot de passe est requis, mais que _lpszOldPassword_ est défini sur null et que l'indicateur MAPI_DIALOG n'est pas défini, **CopyProfile** renvoie MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

