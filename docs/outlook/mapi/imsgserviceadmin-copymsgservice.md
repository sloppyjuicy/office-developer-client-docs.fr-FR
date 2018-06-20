---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784237"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**S’applique à**: Outlook 
  
Copie un service de message dans un profil. 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à copier. 
    
 _lpszDisplayName_
  
> [in] Ce paramètre est déconseillé. 
    
 _lpInterfaceToCopy_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section profil du service de message à copier. Résultats de la transmission NULL dans l’interface de section de profil standard, [IProfSect](iprofsectimapiprop.md), utilisée.
    
 _lpInterfaceDst_
  
> [in] Un pointeur vers l’IID qui représente l’interface à utiliser pour accéder à l’objet indiqué par le paramètre _lpObjectDst_ . Résultats de la transmission NULL dans l’interface de session, [IMAPISession](imapisessioniunknown.md), utilisée. Le paramètre _lpInterfaceDst_ peut également être défini à IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Pointeur vers un pointeur vers un objet d’administration service session ou de message. Le type d’objet doit correspondre à l’identificateur d’interface _lpInterfaceDst_passé. LPMAPISESSION et LPSERVICEADMIN sont des pointeurs d’objet valide.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est copié. Les indicateurs suivants peuvent être définis :
    
SERVICE_UI_ALWAYS 
  
> Demande que le service de message toujours affiche une feuille de propriétés de configuration.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le service de message a été correctement copié.
    
MAPI_E_NO_ACCESS 
  
> Le service de message est déjà dans le profil et n’autorise pas plusieurs instances de lui-même.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** désignés par _lpUID_ ne fait pas référence à un service de message existant. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::CopyMsgService** copie un service de message dans un profil, le profil actif ou un autre profil. Le profil qui contient le service de message à copier et la destination n’ont pas être le même profil, mais ils peuvent être. 
  
Fonction de point d’entrée du service de message n’est pas appelée pour une opération de copie. Le service de message copié a les mêmes paramètres de configuration que l’original. Pour modifier ces paramètres, un client doit appeler la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

