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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cc71974d841005785932cc9017d44c3c0614687d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563386"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre un objet en mode hors connexion basé sur un profil donné.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |Msmapi32.dll  <br/> |
|Appelée par :  <br/> |Client  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
   
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
  
> [in] Ce paramètre n’est pas utilisé. Il doit être 0.
    
 _pwszProfileNameIn_
  
> [in] Le nom du profil qui est l’objet en mode hors connexion. Elle doit être exprimée en Unicode. 
    
 _pGUID_
  
> [in] Pointeur vers un GUID qui peut être utilisé pour identifier cet objet à partir d’autres objets en mode hors connexion. Il doit être **GUID_GlobalState**.
    
 _Conservés_
  
> [in] Ce paramètre n’est pas utilisé. Il doit être **null**.
    
 _ppOfflineObj_
  
> [out] Pointeur vers l’objet demandé en mode hors connexion. L’appelant peut utiliser ce pointeur pour accéder à la [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface pour rechercher les rappels qui prend en charge par cet objet et de définir des rappels pour celui-ci. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L’appel de fonction a réussi.
    
MAPI_E_NOT_FOUND
  
- Échec de l’appel de fonction.
    
## <a name="remarks"></a>Remarques

Il s’agit du premier appel par un client lorsque le client souhaite être averti de toute modification d’état de connexion pour un profil donné. En appelant **HrOpenOfflineObj**, le client obtient un objet en mode hors connexion qui prend en charge **IMAPIOfflineMgr**. Le client peut vérifier les types de rappels pris en charge par l’objet (en utilisant [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), puis configurer les rappels pour qu’il (en utilisant [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
Lorsque vous utilisez [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrOpenOfflineObj@20** comme nom de la procédure. 
  
 **HrOpenOfflineObj** ne fonctionne que pour les clients qui sont des fournisseurs MAPI, compléments COM et les Extensions de Client Exchange en cours d’exécution à l’intérieur du processus Outlook. Dans le cas contraire, **HrOpenOfflineObj** renvoie **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

