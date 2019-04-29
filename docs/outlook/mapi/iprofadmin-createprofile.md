---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404399"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un nouveau profil.
  
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
  
> dans Pointeur vers le nom du nouveau profil.
    
 _lpszPassword_
  
> dans Pointeur vers le mot de passe du nouveau profil. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le profil est créé. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI doit remplir le nouveau profil avec les services de messagerie inclus dans la section [services par défaut] du fichier MAPISVC. inf.
    
MAPI_DIALOG 
  
> Les feuilles de propriétés de configuration de chacun des fournisseurs des services de messagerie à ajouter peuvent être affichées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau profil a été créé.
    
MAPI_E_NO_ACCESS 
  
> Le nouveau profil spécifié existe déjà.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin:: CreateProfile** crée un nouveau profil. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler **CreateProfile** au moment de l'installation de l'application ou à tout moment au cours d'une session. Lorsque cette méthode est appelée au moment de l'installation, la plupart des paramètres de configuration proviennent du fichier de configuration MAPISVC. inf. Lorsque cette méthode est appelée pendant une session active, les paramètres proviennent de l'utilisateur qui est invité via une série de feuilles de propriétés. 
  
Si l'indicateur MAPI_DEFAULT_SERVICES est défini dans le paramètre _ulFlags_ , **CreateProfile** appelle la fonction de point d'entrée du service de messagerie pour chaque service de messagerie dans la section [services par défaut] du fichier MAPISVC. inf. Chaque fonction de point d'entrée de service de messagerie est appelée avec le paramètre _ulContext_ défini sur MSG_SERVICE_CREATE. 
  
Si les deux indicateurs MAPI_DIALOG et MAPI_DEFAULT_SERVICES sont définis, les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d'entrée du service de message. Les fonctions de point d'entrée du service de messagerie sont appelées uniquement après que toutes les informations disponibles du fichier MAPISVC. inf ont été ajoutées au profil. 
  
Le nom du nouveau profil et son mot de passe peuvent contenir jusqu'à 64 caractères et peuvent inclure les caractères suivants:
  
- Tous les caractères alphanumériques, y compris les caractères d'accentuation et le trait de soulignement.
    
- Espaces incorporés, mais pas d'espaces de début ou de fin.
    
Le paramètre _lpszPassword_ doit être null ou un pointeur vers une chaîne de longueur nulle. 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

