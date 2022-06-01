---
title: IMAPISessionAdminServices
description: IMAPISessionAdminServices retourne un pointeur IMsgServiceAdmin pour apporter des modifications aux services de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
ms.openlocfilehash: 4c5c7b254305ce356cf2eb7b5cc3b66ec36e917d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817710"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de messages. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppServiceAdmin_
  
> [out] Pointeur vers un pointeur vers un objet d’administration de service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un pointeur vers un objet d’administration de service de message a été retourné avec succès.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

La méthode **IMAPISession::AdminServices** crée un objet d’administration de service de message, un objet qui prend en charge l’interface **IMsgServiceAdmin** et retourne un pointeur. À l’aide de ce pointeur, vous pouvez appeler **des méthodes IMsgServiceAdmin** pour modifier l’un des services de message dans le profil de session. Sachez que ces modifications ne prennent effet qu’à la session suivante; la session active n’est pas affectée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI utilise la méthode **IMAPISession::AdminServices** pour accéder au profil afin de lire le nom du serveur. |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

