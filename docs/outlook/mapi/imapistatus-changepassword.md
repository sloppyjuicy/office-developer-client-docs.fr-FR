---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783962"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**S’applique à**: Outlook 
  
Modifie le mot de passe d’un fournisseur de services sans afficher l’interface utilisateur. Cette méthode est également pris en charge dans les objets qui implémentent des fournisseurs de services d’état.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpOldPass_
  
> [in] Pointeur vers l’ancien mot de passe.
    
 _lpNewPass_
  
> [in] Pointeur vers le nouveau mot de passe.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le format des mots de passe. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les mots de passe sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les mots de passe sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La modification de mot de passe a réussi.
    
MAPI_E_NO_ACCESS 
  
> L’ancien mot de passe désigné par _lpOldPass_ n’est pas valide. 
    
MAPI_E_NO_SUPPORT 
  
> L’objet état ne gère pas cette opération, comme indiqué par l’absence de l’indicateur STATUS_CHANGE_PASSWORD dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.
    
## <a name="remarks"></a>Remarques

Pas de tous les objets d’état prend en charge la méthode **IMAPIStatus::ChangePassword** . Il est pris en charge uniquement par les fournisseurs de services qui nécessitent des clients entrer un mot de passe. Aucun des objets que MAPI implémente état prend en charge l’opération de modification de mot de passe. 
  
 **ChangePassword** modifie un mot de passe par programmation, sans intervention de l’utilisateur. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Fournisseurs de transport à distance implémentent **ChangePassword** comme indiqué ici. Il n’existe pas de considérations particulières. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

