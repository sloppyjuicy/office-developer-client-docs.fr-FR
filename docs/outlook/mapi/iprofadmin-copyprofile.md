---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c82485e0da5457d069b6248b16b0fc3aa2a95a22
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613799"
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
  
> [in] Pointeur vers le nom du profil à copier.
    
 _lpszOldPassword_
  
> [in] Pointeur vers le mot de passe du profil à copier.
    
 _lpszNewProfileName_
  
> [in] Pointeur vers le nouveau nom du profil copié.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le profil est copié. Les indicateurs suivants peuvent être définies :
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue qui demande à l’utilisateur le mot de passe correct du profil à copier. Si cet indicateur n’est pas définie, aucune boîte de dialogue n’est affichée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le profil a été correctement copié.
    
MAPI_E_ACCESS_DENIED 
  
> Le nouveau nom de profil est identique à celui d’un profil existant.
    
MAPI_E_LOGON_FAILED 
  
> Le mot de passe du profil à copier est incorrect et l’utilisateur n’a pas pu afficher de boîte de dialogue pour demander le mot de passe correct, car MAPI_DIALOG n’a pas été définie dans le paramètre _ulFlags._ 
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::CopyProfile** effectue une copie du profil pointé par  _lpszOldProfileName_, en lui donnant le nom pointé par  _lpszNewProfileName_. La copie d’un profil laisse la copie avec le même mot de passe que l’original.
  
Le nom du profil d’origine, son mot de passe et la copie peuvent comporter jusqu’à 64 caractères et peuvent inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuateur et le caractère de soulignement.
    
- Espaces incorporés, mais pas espaces de début ou de fin.
    
Les mots de passe de profil ne sont pas pris en charge sur tous les systèmes d’exploitation. Sur les systèmes d’exploitation qui ne supportent pas les mots de passe de profil,  _lpszOldPassword_ peut être NULL ou un pointeur vers une chaîne nulle. 
  
Si  _lpszOldPassword_ est définie sur NULL, le profil à copier nécessite un mot de passe et l’indicateur MAPI_DIALOG est définie ; Une boîte de dialogue qui invite l’utilisateur à fournir le mot de passe s’affiche. Si un mot de passe est requis, mais  _que lpszOldPassword_ est définie sur NULL et que l’indicateur MAPI_DIALOG n’est pas définie, **CopyProfile** renvoie MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

