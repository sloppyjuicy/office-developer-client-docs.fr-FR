---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439624"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou définit le profil par défaut d’un client.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil qui deviendra la valeur par défaut, ou NULL. La définition de  _lpszProfileName_ sur NULL indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, ce qui laisse le client sans valeur par défaut. 
    
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

La **méthode IProfAdmin::SetDefaultProfile** établit un profil particulier en tant que profil par défaut du client ou désamorce le profil par défaut actuel. Le profil par défaut est le profil qui est automatiquement utilisé chaque fois que le client commence une session MAPI. **SetDefaultProfile** définit également la propriété PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du nouveau profil par défaut sur TRUE.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour démarrer une session avec le profil par défaut, passez l’MAPI_USE_DEFAULT à la [fonction MAPILogonEx.](mapilogonex.md) 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propriété canonique PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

