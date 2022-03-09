---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
ms.openlocfilehash: 44012b610045ea027c8bbe4a5e7e43a4bfa2f9bb
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375460"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ce paramètre a été supprimé. 
    
 _lpInterfaceToCopy_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil du service de message à copier. La transmission DE NULL entraîne l’utilisation de l’interface de section de profil standard [, IProfSect](iprofsectimapiprop.md).
    
 _lpInterfaceDst_
  
> [in] Pointeur vers l’IID qui représente l’interface à utiliser pour accéder à l’objet pointé par le paramètre  _lpObjectDst_ . Transmission de résultats NULL dans l’interface de session, [IMAPISession](imapisessioniunknown.md), en cours d’utilisation. Le  _paramètre lpInterfaceDst_ peut également être IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Pointeur vers un pointeur vers un objet d’administration de service de session ou de message. Le type d’objet doit correspondre à l’identificateur d’interface transmis  _dans lpInterfaceDst_. Les pointeurs d’objet valides sont LPMAPISESSION et LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est copié. Les indicateurs suivants peuvent être définies :
    
SERVICE_UI_ALWAYS 
  
> Demande au service de message d’afficher toujours une feuille des propriétés de configuration.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de message a été correctement copié.
    
MAPI_E_NO_ACCESS 
  
> Le service de message est déjà dans le profil et n’autorise pas plusieurs instances d’elle-même.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID pointé** par  _lpUID_ ne fait pas référence à un service de message existant. 
    
## <a name="remarks"></a>Remarques

La **méthode IMsgServiceAdmin::CopyMsgService** copie un service de message dans un profil, le profil actif ou un autre profil. Le profil qui contient le service de message à copier et la destination ne doivent pas être du même profil, mais ils peuvent l’être. 
  
La fonction de point d’entrée du service de message n’est pas appelée pour une opération de copie. Le service de message copié a les mêmes paramètres de configuration que son original. Pour modifier ces paramètres, un client doit appeler la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

