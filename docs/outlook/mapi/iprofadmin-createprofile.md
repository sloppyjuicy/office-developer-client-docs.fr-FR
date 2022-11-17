---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8b9316652029bbcf1d81569d60f02b9f8ace53ad
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465015"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un profil.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> [in] Pointeur vers le nom du nouveau profil.
    
 _lpszPassword_
  
> [in] Pointeur vers le mot de passe du nouveau profil. 
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le profil est créé. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFAULT_SERVICES 
  
> MAPI doit remplir le nouveau profil avec les services de message inclus dans la section [Default Services] du fichier Mapisvc.inf.
    
MAPI_DIALOG 
  
> Les feuilles de propriétés de configuration de chacun des fournisseurs dans les services de messagerie à ajouter peuvent être affichées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau profil a été créé.
    
MAPI_E_NO_ACCESS 
  
> Le nouveau profil spécifié existe déjà.
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::CreateProfile** crée un profil. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler **CreateProfile au** moment de l’installation de l’application ou à tout moment pendant une session. Lorsque cette méthode est appelée au moment de l’installation, la plupart des paramètres de configuration proviennent du fichier de configuration Mapisvc.inf. Lorsque cette méthode est appelée au cours d’une session active, les paramètres proviennent de l’utilisateur qui est invité par le biais d’une série de feuilles de propriétés. 
  
Si l’indicateur MAPI_DEFAULT_SERVICES est définie dans le paramètre _ulFlags_ , **CreateProfile** appelle la fonction de point d’entrée de service de message pour chaque service de message dans la section [Default Services] du fichier Mapisvc.inf. Chaque fonction de point d’entrée de service de message est appelée avec le  _paramètre ulContext_ MSG_SERVICE_CREATE. 
  
Si les indicateurs MAPI_DIALOG et MAPI_DEFAULT_SERVICES sont tous deux définies, les valeurs des paramètres _ulUIParam_ et  _ulFlags sont également transmises_ à la fonction de point d’entrée du service de message. Les fonctions de point d’entrée du service de message sont appelées uniquement une fois que toutes les informations disponibles du fichier Mapisvc.inf ont été ajoutées au profil. 
  
Le nom du nouveau profil et son mot de passe peuvent comporter jusqu’à 64 caractères et inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuateur et le caractère de soulignement.
    
- Espaces incorporés, mais pas espaces de début ou de fin.
    
Le  _paramètre lpszPassword_ doit être NULL ou pointeur vers une chaîne de longueur nulle. 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

