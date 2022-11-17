---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9ca37dfd25eeed3a9bef6961a88bc7c5a74e0311
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465008"
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
  
> Le profil a été supprimé avec succès.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::D eleteProfile** supprime un profil. Si le profil à supprimer est en cours d’utilisation lorsque **DeleteProfile** est appelé, **DeleteProfile** renvoie S_OK mais ne supprime pas immédiatement le profil. Au lieu de cela, **DeleteProfile** marque le profil à supprimer et le supprime une fois qu’il n’est plus utilisé, une fois toutes ses sessions actives terminées. 
  
La fonction de point d’entrée pour chaque service de message dans le profil est appelée avec la valeur MSG_SERVICE_DELETE définie dans _le paramètre ulContext_ . Tout d’abord, la fonction supprime le service, puis supprime la section de profil du service. La fonction de point d’entrée du service de message n’est pas rappelée après la suppression du service. 
  
Aucun mot de passe n’est requis pour supprimer un profil.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI utilise **la méthode IProfAdmin::D eleteProfile** pour supprimer le profil sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

