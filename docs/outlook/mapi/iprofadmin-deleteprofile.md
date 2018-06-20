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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784390"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**S’applique à**: Outlook 
  
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
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le profil a été supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::DeleteProfile** supprime un profil. Si le profil à supprimer est en cours d’utilisation lorsque **DeleteProfile** est appelée, **DeleteProfile** renvoie S_OK mais ne supprime pas le profil immédiatement. Au lieu de cela, **DeleteProfile** marque le profil de suppression et le supprime une fois qu’il est n’est plus utilisé, lorsque toutes les sessions actives sont terminées. 
  
La fonction de point d’entrée pour chaque service de message dans le profil est appelée avec la valeur MSG_SERVICE_DELETE définie dans le paramètre _ulContext_ . Tout d’abord, la fonction supprime le service, puis il supprime la section de profil du service. La fonction de point d’entrée de message service n’est pas encore appelée une fois que le service a été supprimé. 
  
Aucun mot de passe n’est requis pour supprimer un profil.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin::DeleteProfile** pour supprimer le profil sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

