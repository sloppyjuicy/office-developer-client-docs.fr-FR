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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428745"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre une description d’un formulaire particulier dans un fichier de configuration.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameters

 _szFileName_
  
> [in] Chaîne qui nomme le fichier de message de description du formulaire dans lequel sa description est enregistrée. Ce nom de fichier doit avoir l’extension .fdm.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_EXTENDED_ERROR 
  
> Le fichier de configuration n’a pas pu être écrit. Pour obtenir la structure [MAPIERROR](mapierror.md) associée à l’erreur, appelez la méthode [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm a** probablement été appelé pour enregistrer un formulaire dans le conteneur de formulaire local. **SaveForm n’est** pas pris en charge sur le conteneur de formulaire local. 
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormInfo::SaveForm** pour enregistrer une description du formulaire actuel dans le fichier qui a le nom de fichier donné. **SaveForm crée** un fichier de configuration. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez réinstaller les formulaires en les sélectionnant dans une liste de messages de descripteur de formulaire dans une boîte de dialogue que les fournisseurs de bibliothèque de formulaires affichent. L’extension recommandée pour les messages descripteur de formulaire est .fdm.
  
Appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) si **SaveForm** renvoie MAPI_E_EXTENDED_ERROR et vérifiez la structure **MAPIERROR** renvoyée pour déterminer la condition à l’origine de l’erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

