---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420240"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé. Modifie le mot de passe d'un profil.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpszProfileName_
  
> dans Pointeur vers le nom du profil associé au mot de passe à modifier.
    
 _lpszOldPassword_
  
> dans Pointeur vers le mot de passe actuel.
    
 _lpszNewPassword_
  
> dans Pointeur vers le nouveau mot de passe.
    
 _ulFlags_
  
> dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Le nom du profil et les mots de passe sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, ces chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Si cette méthode est appelée, elle renverra S_OK. Toutefois, aucune action n'est effectuée.
    
## <a name="remarks"></a>Remarques

N'utilisez pas cette méthode. MAPI ne prend pas en charge les mots de passe des profils.
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

