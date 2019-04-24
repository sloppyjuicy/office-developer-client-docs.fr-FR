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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309596"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d'accéder à un objet d'administration de service de messagerie pour apporter des modifications aux services de messagerie dans un profil.
  
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
  
> dans Pointeur vers le nom du profil à modifier. Le paramètre _lpszProfileName_ ne doit pas être null. 
    
 _lpszPassword_
  
> dans Toujours NULL. 
    
 _ulUIParam_
  
> dans Un handle de la fenêtre parente pour les boîtes de dialogue ou les fenêtres que cette méthode affiche.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la récupération de l'objet d'administration du service de messagerie. Les indicateurs suivants peuvent être définis:
    
MAPI_DIALOG 
  
> Active l'affichage d'une interface utilisateur. 
    
MAPI_UNICODE 
  
> Le nom du profil est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le nom est au format ANSI.
    
 _lppServiceAdmin_
  
> remarquer Pointeur vers un pointeur vers un objet d'administration de service de messagerie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet d'administration du service de messagerie a été renvoyé.
    
MAPI_E_LOGON_FAILED 
  
> Le profil spécifié n'existe pas ou le mot de passe est incorrect et aucune boîte de dialogue n'a pu être affichée pour demander le mot de passe correct car MAPI_DIALOG n'a pas été défini dans _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin:: AdminServices** permet d'accéder à un objet d'administration du service de messagerie pour apporter des modifications à la configuration des services de messagerie dans un profil. 
  
 Le paramètre _lpszPassword_ doit être null ou un pointeur vers une chaîne de longueur nulle. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Bien que vous puissiez récupérer un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) en appelant cette méthode ou [IMAPISession:: AdminServices](imapisession-adminservices.md), appelez **IProfAdmin:: AdminServices** si vous disposez strictement d'un client de configuration et que vous n'avez pas besoin de fonctionnalités de messagerie. **IProfAdmin:: AdminServices** ne crée pas d'objet session et ne charge pas de fournisseurs de services, ce qui améliore les performances. 
  
Vous ne pouvez pas utiliser **IProfAdmin:: AdminServices** pour créer un profil. Par conséquent, vous devez spécifier un profil valide existant dans _lpszProfileName_. Si le profil spécifié n'existe pas, **IProfAdmin:: AdminServices** renvoie MAPI_E_LOGON_FAILED. 
  
Le nom du profil peut contenir jusqu'à 64 caractères et peut contenir les caractères suivants:
  
- Tous les caractères alphanumériques, y compris les caractères d'accentuation et le trait de soulignement. 
    
- Espaces incorporés, mais pas d'espaces de début ou de fin.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin:: AdminServices** pour ouvrir un objet d'administration de service de messagerie pour le profil sélectionné et ajouter des services.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

