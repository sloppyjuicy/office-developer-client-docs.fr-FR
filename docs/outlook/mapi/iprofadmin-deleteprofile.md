---
title: IProfAdminDeleteProfile
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IProfAdmin DeleteProfile, qui supprime un profil.
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
ms.openlocfilehash: 40e2e54e6307159327ebc190914b427b078b8d44
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826910"
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

La méthode **IProfAdmin::D eleteProfile** supprime un profil. Si le profil à supprimer est utilisé lorsque **DeleteProfile** est appelé, **DeleteProfile** retourne S_OK mais ne supprime pas immédiatement le profil. Au lieu de cela, **DeleteProfile** marque le profil pour suppression et le supprime une fois qu’il n’est plus utilisé, lorsque toutes ses sessions actives ont pris fin. 
  
La fonction de point d’entrée pour chaque service de message dans le profil est appelée avec la valeur MSG_SERVICE_DELETE définie dans le paramètre _ulContext_ . Tout d’abord, la fonction supprime le service, puis supprime la section de profil du service. La fonction de point d’entrée du service de message n’est plus appelée une fois le service supprimé. 
  
Aucun mot de passe n’est requis pour supprimer un profil.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI utilise la méthode **IProfAdmin::D eleteProfile** pour supprimer le profil sélectionné. |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

