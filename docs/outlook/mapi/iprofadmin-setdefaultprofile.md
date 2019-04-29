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
  
Définit ou efface le profil par défaut d'un client.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> dans Pointeur vers le nom du profil qui deviendra la valeur par défaut, ou NULL. La définition de _lpszProfileName_ sur null indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, en laissant le client sans valeur par défaut. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de la chaîne désignée par _lpszProfileName_. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Le nom du profil est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du profil est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un profil par défaut a été correctement établi ou supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n'existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin:: SetDefaultProfile** établit un profil particulier en tant que profil par défaut du client ou efface le profil par défaut actuel. Le profil par défaut est le profil qui est utilisé automatiquement chaque fois que le client lance une session MAPI. **SetDefaultProfile** définit également la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du profil par défaut sur true.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour démarrer une session avec le profil par défaut, transmettez l'indicateur MAPI_USE_DEFAULT à la fonction [MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propriété canonique PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

