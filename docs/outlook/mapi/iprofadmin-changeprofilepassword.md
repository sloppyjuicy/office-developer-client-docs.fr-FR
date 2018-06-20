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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784384"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**S’applique à**: Outlook 
  
Déconseillé. Modifie le mot de passe pour un profil.
  
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
  
> [in] Pointeur vers le nom du profil associé avec le mot de passe à modifier.
    
 _lpszOldPassword_
  
> [in] Pointeur vers le mot de passe actuel.
    
 _lpszNewPassword_
  
> [in] Pointeur vers le nouveau mot de passe.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Le nom de profil et les mots de passe sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Si cette méthode est appelée, elle renvoie S_OK. Toutefois, aucune action ne sera entreprise.
    
## <a name="remarks"></a>Remarques

N’utilisez pas cette méthode. MAPI ne gère pas les mots de passe pour les profils.
  
## <a name="see-also"></a>Voir aussi



[IProfAdmin : IUnknown](iprofadminiunknown.md)

