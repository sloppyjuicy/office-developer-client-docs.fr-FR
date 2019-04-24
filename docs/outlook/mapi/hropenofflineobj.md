---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347746"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet hors connexion basé sur un profil donné.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par:  <br/> |msmapi32. dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>Paramètres

 _ulReserved_
  
> dans Ce paramètre n'est pas utilisé. Il doit être égal à 0.
    
 _pwszProfileNameIn_
  
> dans Nom du profil pour lequel l'objet hors connexion est destiné. Il doit être exprimé en Unicode. 
    
 _pGUID_
  
> dans Pointeur vers un GUID qui peut être utilisé pour identifier cet objet de manière unique à partir d'autres objets hors connexion. Il doit être **GUID_GlobalState**.
    
 _Disparition_
  
> dans Ce paramètre n'est pas utilisé. Elle doit être **null**.
    
 _ppOfflineObj_
  
> remarquer Pointeur vers l'objet hors connexion demandé. L'appelant peut utiliser ce pointeur pour accéder à l'interface [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) pour rechercher les rappels pris en charge par cet objet et pour configurer des rappels pour celui-ci. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L'appel de fonction est réussi.
    
MAPI_E_NOT_FOUND
  
- Échec de l'appel de la fonction.
    
## <a name="remarks"></a>Remarques

Il s'agit du premier appel qu'un client effectue lorsque le client souhaite être informé des modifications d'état de connexion pour un profil donné. Lors de l'appel de **HrOpenOfflineObj**, le client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. Le client peut vérifier les genres de rappels pris en charge par l'objet (à l'aide de [IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)), puis configurer des rappels pour lui (à l'aide de [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).
  
Lors de l'utilisation de [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) pour Rechercher l'adresse de cette fonction dans msmapi32. dll, spécifiez **HrOpenOfflineObj @ 20** comme nom de procédure. 
  
 **HrOpenOfflineObj** fonctionne uniquement pour les clients qui sont des fournisseurs MAPI, des compléments COM et des extensions client Exchange en cours d'exécution dans le processus Outlook. Sinon, **HrOpenOfflineObj** renvoie **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

