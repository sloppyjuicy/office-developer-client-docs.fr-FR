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
ms.openlocfilehash: 92d5dcdf3e5e3fbdb7490d777a24976c9ae4af1a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582790"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Pointeur vers le nom du nouveau profil.
    
 _lpszPassword_
  
> [in] Pointeur vers le mot de passe du nouveau profil. 
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le profil est créé. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFAULT_SERVICES 
  
> MAPI doit remplir le nouveau profil avec les services de message qui sont inclus dans la section [Services par défaut] du fichier Mapisvc.inf.
    
MAPI_DIALOG 
  
> Vous pouvez afficher les feuilles de propriétés de configuration de chacun des fournisseurs dans les services de messagerie à ajouter. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le nouveau profil a été créé.
    
MAPI_E_NO_ACCESS 
  
> Le nouveau profil spécifié existe déjà.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::CreateProfile** crée un nouveau profil. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez appeler **CreateProfile** au moment de l’installation ou à tout moment pendant une session. Lorsque cette méthode est appelée au moment de l’installation, la plupart des paramètres de configuration proviennent de configuration du fichier Mapisvc.inf. Lorsque cette méthode est appelée lors d’une session active, les paramètres proviennent de l’utilisateur est invité à travers une série de feuilles de propriétés. 
  
Si l’indicateur MAPI_DEFAULT_SERVICES est défini dans le paramètre _ulFlags_ , **CreateProfile** appelle la fonction de point d’entrée de message service pour chaque service de message dans la section [Services par défaut] dans le fichier Mapisvc.inf. Chaque fonction de point d’entrée de message service est appelée avec le paramètre _ulContext_ défini sur MSG_SERVICE_CREATE. 
  
Si indicateurs MAPI_DIALOG et de MAPI_DEFAULT_SERVICES sont définies, les valeurs dans les paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d’entrée de message service. Les fonctions de point d’entrée de message service sont appelées uniquement une fois que toutes les informations disponibles à partir du fichier Mapisvc.inf a été ajoutées au profil. 
  
Le nom du nouveau profil et son mot de passe peut être jusqu'à 64 caractères et peut inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement.
    
- Des espaces, mais pas espaces à gauche ou.
    
Le paramètre _lpszPassword_ doit être NULL ou un pointeur vers une chaîne de longueur nulle. 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

