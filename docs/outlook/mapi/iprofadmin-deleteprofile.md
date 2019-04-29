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
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419589"
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
  
> dans Pointeur vers le nom du profil à supprimer.
    
 _ulFlags_
  
> dans Toujours NULL. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le profil a été supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n'existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **eleteprofile::D** supprime un profil. Si le profil à supprimer est en cours d'utilisation lors de l'appel de **DeleteProfile** , **DeleteProfile** retourne S_OK mais ne supprime pas le profil immédiatement. Au lieu de cela, **DeleteProfile** marque le profil pour suppression et le supprime une fois qu'il n'est plus utilisé, lorsque toutes ses sessions actives sont terminées. 
  
La fonction de point d'entrée pour chaque service de messagerie dans le profil est appelée avec la valeur MSG_SERVICE_DELETE définie dans le paramètre _ulContext_ . Tout d'abord, la fonction supprime le service, puis supprime la section de profil du service. La fonction de point d'entrée du service de messagerie n'est pas rappelée une fois que le service a été supprimé. 
  
Aucun mot de passe n'est requis pour supprimer un profil.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin::D eleteprofile** pour supprimer le profil sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

