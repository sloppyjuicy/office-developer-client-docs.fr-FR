---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
ms.openlocfilehash: e2ecf796899dde4453ce6f94101873f43de0733d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370244"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou effacer le profil par défaut d’un client.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil qui deviendra la valeur par défaut, ou NULL. La  _définition de lpszProfileName_ sur NULL indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, ce qui laisse le client sans valeur par défaut. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de la chaîne pointée par  _lpszProfileName_. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Le nom du profil est au format Unicode. Si l MAPI_UNICODE n’est pas définie, le nom du profil est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un profil par défaut a été correctement établi ou supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::SetDefaultProfile** établit un profil particulier en tant que profil par défaut du client ou désinsaisie le profil par défaut actuel. Le profil par défaut est le profil qui est automatiquement utilisé chaque fois que le client commence une session MAPI. **SetDefaultProfile** définit également la propriété **PR_DEFAULT_PROFILE (**[PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du nouveau profil par défaut sur TRUE.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour démarrer une session avec le profil par défaut, passez l’MAPI_USE_DEFAULT à la [fonction MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propriété canonique PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

