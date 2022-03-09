---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
ms.openlocfilehash: a0b8cddfd14620df13f07030d05af3d7a211f834
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370308"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé. Modifie le mot de passe d’un profil.
  
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
  
> [in] Pointeur vers le nom du profil associé au mot de passe à modifier.
    
 _lpszOldPassword_
  
> [in] Pointeur vers le mot de passe actuel.
    
 _lpszNewPassword_
  
> [in] Pointeur vers le nouveau mot de passe.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes transmises. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Le nom de profil et les mots de passe sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, ces chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Si cette méthode est appelée, elle S_OK. Toutefois, aucune action n’est prise.
    
## <a name="remarks"></a>Remarques

N’utilisez pas cette méthode. MAPI ne prend pas en charge les mots de passe pour les profils.
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

