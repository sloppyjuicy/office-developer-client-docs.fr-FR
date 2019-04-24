---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321713"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre une description d'un formulaire particulier dans un fichier de configuration.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Paramètres

 _szFileName_
  
> dans Chaîne qui nomme le fichier de message Description du formulaire où sa description est enregistrée. Ce nom de fichier doit être doté de l'extension. FDM.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_EXTENDED_ERROR 
  
> Le fichier de configuration n'a pas pu être écrit. Pour obtenir la structure [MAPIERROR](mapierror.md) associée à l'erreur, appelez la méthode [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** a probablement été appelé pour enregistrer un formulaire dans le conteneur de formulaire local. **SaveForm** n'est pas pris en charge sur le conteneur de formulaire local. 
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormInfo:: saveForm** pour enregistrer une description du formulaire actif dans le fichier portant le nom de fichier donné. **SaveForm** crée un fichier de configuration. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez réinstaller les formulaires en les sélectionnant dans la liste des messages du descripteur de formulaire dans une boîte de dialogue qui s'affiche dans les fournisseurs de bibliothèques de formulaires. L'extension recommandée pour les messages du descripteur de formulaire est. FDM.
  
Appelez la méthode [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) si **saveForm** renvoie MAPI_E_EXTENDED_ERROR et vérifiez la structure **MAPIERROR** renvoyée pour déterminer la condition à l'origine de l'erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

