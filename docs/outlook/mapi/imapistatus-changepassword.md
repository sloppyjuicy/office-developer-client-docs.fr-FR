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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410356"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie le mot de passe d'un fournisseur de services sans afficher d'interface utilisateur. Cette méthode est éventuellement prise en charge dans les objets d'État implémentés par les fournisseurs de services.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpOldPass_
  
> dans Pointeur vers l'ancien mot de passe.
    
 _lpNewPass_
  
> dans Pointeur vers le nouveau mot de passe.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le format des mots de passe. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les mots de passe sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les mots de passe sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La modification du mot de passe a réussi.
    
MAPI_E_NO_ACCESS 
  
> L'ancien mot de passe désigné par _lpOldPass_ n'est pas valide. 
    
MAPI_E_NO_SUPPORT 
  
> L'objet Status ne prend pas en charge cette opération, comme indiqué par l'absence de l'indicateur STATUS_CHANGE_PASSWORD dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l'objet Status.
    
## <a name="remarks"></a>Remarques

Tous les objets d'État ne prennent pas en charge la méthode **IMAPIStatus:: ChangePassword** . Il est pris en charge uniquement par les fournisseurs de services qui nécessitent des clients pour entrer un mot de passe. Aucun des objets d'État que MAPI implémente ne prend en charge l'opération de modification de mot de passe. 
  
 **ChangePassword** modifie un mot de passe par programme, sans intervention de l'utilisateur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de transport à distance implémentent **ChangePassword** comme indiqué ici. Il n'y a aucune considération particulière. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

