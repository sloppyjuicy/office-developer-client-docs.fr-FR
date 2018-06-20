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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783948"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**S’applique à**: Outlook 
  
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
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Un pointeur vers un objet d’administration service message a été renvoyé avec succès.
    
## <a name="notes-to-callers"></a>Notes aux appelants

La méthode **IMAPISession::AdminServices** crée un objet d’administration service message, un objet qui prend en charge l’interface **IMsgServiceAdmin** et retourne un pointeur. À l’aide de ce pointeur, vous pouvez appeler des méthodes de **IMsgServiceAdmin** pour modifier les services de messagerie dans le profil de la session. Sachez que ces modifications ne prendront effet jusqu'à la prochaine session ; la session en cours n’est pas affectée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI utilise la méthode **IMAPISession::AdminServices** pour accéder au profil pour lire le nom du serveur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

