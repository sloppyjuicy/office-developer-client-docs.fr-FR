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
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593472"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Enregistre une description d’un formulaire particulier dans un fichier de configuration.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Paramètres

 _szFileName_
  
> [in] Chaîne qui nomme le fichier de message de description du formulaire où sa description est enregistrée. Ce nom de fichier doit avoir l’extension .fdm.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_EXTENDED_ERROR 
  
> Le fichier de configuration n’a pas pu être écrites. Pour obtenir la structure [MAPIERROR](mapierror.md) qui est associée à l’erreur, appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** a été appelée probablement pour enregistrer un formulaire dans le conteneur de formulaire local. **SaveForm** n’est pas pris en charge sur le conteneur de formulaire local. 
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **IMAPIFormInfo::SaveForm** pour enregistrer une description du formulaire actif dans le fichier portant le nom de fichier donné. **SaveForm** crée un fichier de configuration. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez réinstaller les formulaires en les sélectionnant à partir d’une liste de formulaire descripteur messages dans une boîte de dialogue Affichage de fournisseurs de bibliothèque de formulaires. L’extension recommandée pour les messages de descripteur de formulaire est .fdm.
  
Appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) si **SaveForm** renvoie MAPI_E_EXTENDED_ERROR et vérifiez la structure **MAPIERROR** retournée pour déterminer la condition qui a provoqué l’erreur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

