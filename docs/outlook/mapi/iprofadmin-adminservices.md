---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a9e596ff8561d5aabc71ffe3540efaeef8f5b83d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593983"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Donne accès à un objet de l’administration de service de message pour apporter des modifications aux services de message dans un profil.
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil à modifier. Le paramètre _lpszProfileName_ ne doit pas être NULL. 
    
 _lpszPassword_
  
> [in] Toujours NULL. 
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente pour les boîtes de dialogue ou windows qui affiche cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la récupération de l’objet de l’administration du service de message. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Active l’affichage d’une interface utilisateur. 
    
MAPI_UNICODE 
  
> Le nom de profil est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le nom est au format ANSI.
    
 _lppServiceAdmin_
  
> [out] Pointeur vers un pointeur vers un objet de l’administration de service de message.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’objet de l’administration du service de message a été renvoyée avec succès.
    
MAPI_E_LOGON_FAILED 
  
> Le profil spécifié n’existe pas, ou le mot de passe est incorrecte et une boîte de dialogue ne peut pas être affichée à l’utilisateur de demander le mot de passe, car MAPI_DIALOG n’a pas été défini dans _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::AdminServices** permet d’accéder à un objet de l’administration de service de message pour apporter des modifications de configuration pour les services de messagerie dans un profil. 
  
 Le paramètre _lpszPassword_ doit être NULL ou un pointeur vers une chaîne de longueur nulle. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Bien que vous pouvez récupérer un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) en appelant cette méthode ou [IMAPISession::AdminServices](imapisession-adminservices.md), appelez **IProfAdmin::AdminServices** si vous avez strictement un client de configuration et n’offre aucune des fonctionnalités de messagerie. **IProfAdmin::AdminServices** ne crée pas d’un objet de la session et ne se charge pas les fournisseurs de services, ce qui améliore les performances. 
  
Vous ne pouvez pas utiliser **IProfAdmin::AdminServices** pour créer un profil. Par conséquent, vous devez spécifier un profil existant valid dans _lpszProfileName_. Si le profil spécifié n’existe pas, **IProfAdmin::AdminServices** renvoie MAPI_E_LOGON_FAILED. 
  
Le nom du profil peut être jusqu'à 64 caractères et peut inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement. 
    
- Des espaces, mais pas espaces à gauche ou.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin::AdminServices** pour ouvrir un objet de l’administration de service de message pour le profil sélectionné Ajouter des services.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

