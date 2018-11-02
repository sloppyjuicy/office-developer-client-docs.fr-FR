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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9e22111ec920d89e0874baf71946681c204cacd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571205"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie d’un profil.
  
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le profil est copié. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue qui invite l’utilisateur pour le mot de passe du profil à copier. Si cet indicateur n’est pas défini, aucune boîte de dialogue ne s’affiche.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le profil a été correctement copié.
    
MAPI_E_ACCESS_DENIED 
  
> Le nom du nouveau profil est identique à celui d’un profil existant.
    
MAPI_E_LOGON_FAILED 
  
> Le mot de passe pour le profil à copier est incorrect, et une boîte de dialogue ne peut pas être affichée à l’utilisateur de demander le mot de passe, car MAPI_DIALOG n’a pas été défini dans le paramètre _ulFlags_ . 
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::CopyProfile** effectue une copie du profil désigné par _lpszOldProfileName_, en lui donnant le nom désignée par _lpszNewProfileName_. Copie d’un profil laisse la copie avec le même mot de passe d’origine.
  
Le nom de la copie du profil d’origine et son mot de passe peut être jusqu'à 64 caractères et peut inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement.
    
- Des espaces, mais pas espaces à gauche ou.
    
Profil des mots de passe ne sont pas pris en charge sur tous les systèmes d’exploitation. Sur les systèmes d’exploitation qui ne prennent pas en charge les mots de passe de profil, _lpszOldPassword_ peut être NULL ou un pointeur vers une chaîne de longueur nulle. 
  
Si _lpszOldPassword_ est défini sur NULL, le profil doit être copié requiert un mot de passe, et l’indicateur MAPI_DIALOG est défini ; une boîte de dialogue qui invite l’utilisateur à fournir le mot de passe s’affiche. Si un mot de passe est requis, mais _lpszOldPassword_ est définie sur NULL et l’indicateur MAPI_DIALOG n’est pas défini, **CopyProfile** renvoie MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

