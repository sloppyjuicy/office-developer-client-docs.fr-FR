---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aa3c010eafeba7908498965bc0491c993a4a9120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572084"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un profil.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil à supprimer.
    
 _ulFlags_
  
> [in] Toujours NULL. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le profil a été supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::DeleteProfile** supprime un profil. Si le profil à supprimer est en cours d’utilisation lorsque **DeleteProfile** est appelée, **DeleteProfile** renvoie S_OK mais ne supprime pas le profil immédiatement. Au lieu de cela, **DeleteProfile** marque le profil de suppression et le supprime une fois qu’il est n’est plus utilisé, lorsque toutes les sessions actives sont terminées. 
  
La fonction de point d’entrée pour chaque service de message dans le profil est appelée avec la valeur MSG_SERVICE_DELETE définie dans le paramètre _ulContext_ . Tout d’abord, la fonction supprime le service, puis il supprime la section de profil du service. La fonction de point d’entrée de message service n’est pas encore appelée une fois que le service a été supprimé. 
  
Aucun mot de passe n’est requis pour supprimer un profil.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin::DeleteProfile** pour supprimer le profil sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

