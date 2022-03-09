---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
ms.openlocfilehash: ff0de6776f440d6232dcc4d8c743386c2a4509da
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368845"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie le mot de passe d’un fournisseur de services sans afficher d’interface utilisateur. Cette méthode est éventuellement prise en charge dans les objets d’état implémentés par les fournisseurs de services.
  
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
  
> [in] Masque de bits d’indicateurs qui contrôle le format des mots de passe. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les mots de passe sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les mots de passe sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La modification du mot de passe a réussi.
    
MAPI_E_NO_ACCESS 
  
> L’ancien mot de passe pointé par  _lpOldPass_ n’est pas valide. 
    
MAPI_E_NO_SUPPORT 
  
> L’objet status ne prend pas en charge cette opération, comme indiqué par l’absence de l’indicateur STATUS_CHANGE_PASSWORD dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.
    
## <a name="remarks"></a>Remarques

Les objets d’état ne sont pas tous en charge par la méthode **IMAPIStatus::ChangePassword** . Il est uniquement pris en charge par les fournisseurs de services qui exigent que les clients entrent un mot de passe. Aucun des objets d’état implémentés par MAPI ne permet de modifier le mot de passe. 
  
 **ChangePassword** modifie un mot de passe par programme, sans intervention de l’utilisateur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de transport distant **implémentent ChangePassword** comme indiqué ici. Il n’existe aucune considération particulière. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

