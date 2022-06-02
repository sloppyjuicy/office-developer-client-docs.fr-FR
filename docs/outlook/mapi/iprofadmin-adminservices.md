---
title: IProfAdminAdminServices
description: IProfAdmin AdminServices fournit l’accès à un objet d’administration de service de message pour apporter des modifications aux services de message dans un profil.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
ms.openlocfilehash: 0f19205713754f5d6e85be59b6ba89f6ff37a05f
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828531"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à un objet d’administration de service de message pour apporter des modifications aux services de message dans un profil.
  
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
  
> [in] Pointeur vers le nom du profil à modifier. Le paramètre  _lpszProfileName_ ne doit pas être NULL. 
    
 _lpszPassword_
  
> [in] Toujours NULL. 
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente pour toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la récupération de l’objet d’administration du service de message. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Active l’affichage d’une interface utilisateur. 
    
MAPI_UNICODE 
  
> Le nom du profil est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, le nom est au format ANSI.
    
 _lppServiceAdmin_
  
> [out] Pointeur vers un pointeur vers un objet d’administration de service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet d’administration du service de message a été retourné avec succès.
    
MAPI_E_LOGON_FAILED 
  
> Le profil spécifié n’existe pas, ou le mot de passe était incorrect et une boîte de dialogue n’a pas pu être affichée à l’utilisateur pour demander le mot de passe correct, car MAPI_DIALOG n’a pas été définie dans  _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::AdminServices permet d’accéder** à un objet d’administration de service de message pour apporter des modifications de configuration aux services de messages dans un profil. 
  
 Le paramètre  _lpszPassword_ doit être NULL ou un pointeur vers une chaîne de longueur nulle. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Bien que vous puissiez récupérer un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) en appelant cette méthode ou [IMAPISession::AdminServices](imapisession-adminservices.md), appelez **IProfAdmin::AdminServices** si vous avez strictement un client de configuration et n’offrez aucune fonctionnalité de messagerie. **IProfAdmin::AdminServices** ne crée pas d’objet de session et ne charge aucun fournisseur de services, ce qui améliore les performances. 
  
Vous ne pouvez pas utiliser **IProfAdmin::AdminServices** pour créer un profil. Par conséquent, vous devez spécifier un profil valide existant dans  _lpszProfileName_. Si le profil spécifié n’existe pas, **IProfAdmin::AdminServices** retourne MAPI_E_LOGON_FAILED. 
  
Le nom du profil peut contenir jusqu’à 64 caractères et peut inclure les caractères suivants :
  
- Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement. 
    
- Espaces incorporés, mais pas espaces de début ou de fin.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin::AdminServices** pour ouvrir un objet d’administration de service de message pour le profil sélectionné afin d’ajouter des services. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

