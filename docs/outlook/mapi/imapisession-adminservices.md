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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322413"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de messagerie. 
  
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
  
> remarquer Pointeur vers un pointeur vers un objet d'administration de service de messagerie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un pointeur vers un objet d'administration de service de message a été renvoyé.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

La méthode **IMAPISession:: AdminServices** crée un objet d'administration de service de messagerie, un objet qui prend en charge l'interface **IMsgServiceAdmin** et renvoie un pointeur. À l'aide de ce pointeur, vous pouvez appeler des méthodes **IMsgServiceAdmin** pour modifier les services de messagerie dans le profil de session. N'oubliez pas que ces modifications ne prennent effet qu'au cours de la session suivante; la session en cours n'est pas affectée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |GetServerName  <br/> |MFCMAPI utilise la méthode **IMAPISession:: AdminServices** pour accéder au profil afin de lire le nom du serveur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

