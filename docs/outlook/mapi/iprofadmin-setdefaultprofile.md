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
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587704"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Active ou désactive le profil par défaut d’un client.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil qui deviennent les valeurs par défaut, ou NULL. Définition de _lpszProfileName_ sur NULL indique que **SetDefaultProfile** doit supprimer le profil par défaut existant, quitter le client sans valeur par défaut. 
    
 _ulFlags_
  
> [in] Un masque de bits d’indicateurs qui contrôle le type de la chaîne indiquée par _lpszProfileName_. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Le nom de profil est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le nom de profil est au format ANSI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Un profil par défaut a été correctement établi ou supprimé.
    
MAPI_E_NOT_FOUND 
  
> Le profil spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::SetDefaultProfile** établit un profil spécifique comme le profil du client par défaut ou efface le profil par défaut actuel. Le profil par défaut est le profil qui est utilisé automatiquement chaque fois que le client commence une session MAPI. **SetDefaultProfile** définit également une propriété de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) du nouveau profil par défaut la valeur True.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour démarrer une session avec le profil par défaut, passez l’indicateur MAPI_USE_DEFAULT à la fonction [MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propriété canonique PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

