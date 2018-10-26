---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cb7fa7bb7dc17a89fc7cc40ae370accc40fa3941
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579837"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications à des services de messagerie. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lppServiceAdmin_
  
> [out] Pointeur vers un pointeur vers un objet de l’administration de service de message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un pointeur vers un objet d’administration service message a été renvoyé avec succès.
    
## <a name="notes-to-callers"></a>Notes aux appelants

La méthode **IMAPISession::AdminServices** crée un objet d’administration service message, un objet qui prend en charge l’interface **IMsgServiceAdmin** et retourne un pointeur. À l’aide de ce pointeur, vous pouvez appeler des méthodes de **IMsgServiceAdmin** pour modifier les services de messagerie dans le profil de la session. Sachez que ces modifications ne prendront effet jusqu'à la prochaine session ; la session en cours n’est pas affectée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI utilise la méthode **IMAPISession::AdminServices** pour accéder au profil pour lire le nom du serveur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

