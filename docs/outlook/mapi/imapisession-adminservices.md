---
title: IMAPISessionAdminServices
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4d7fe66f58e84e689b082c90898c60b98453f6af
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784054"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un [pointeur IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de message. 
  
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
  
> Un pointeur vers un objet d’administration de service de message a été renvoyé avec succès.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

La **méthode IMAPISession::AdminServices** crée un objet d’administration de service de message, un objet qui prend en charge l’interface **IMsgServiceAdmin** et renvoie un pointeur. À l’aide de ce pointeur, vous pouvez appeler des méthodes **IMsgServiceAdmin** pour modifier les services de message dans le profil de session. N’ignorez pas que ces modifications ne prennent effet qu’après la session suivante . la session en cours n’est pas affectée. 
  
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

