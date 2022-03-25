---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: edd2b6610ddc0aa83b59608f077966b3639ed3dd
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720257"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet hors connexion basé sur un profil donné.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
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
  
> [in] Ce paramètre n’est pas utilisé. Elle doit être 0.
    
 _pwszProfileNameIn_
  
> [in] Nom du profil pour l’objet hors connexion. Elle doit être exprimée en Unicode. 
    
 _pGUID_
  
> [in] Pointeur vers un GUID qui peut être utilisé pour identifier de manière unique cet objet à partir d’autres objets hors connexion. Elle doit être **GUID_GlobalState**.
    
 _pReserved_
  
> [in] Ce paramètre n’est pas utilisé. Elle doit être **null**.
    
 _ppOfflineObj_
  
> [out] Pointeur vers l’objet hors connexion demandé. L’appelant peut utiliser ce pointeur pour accéder à l’interface [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) pour rechercher les rappels pris en charge par cet objet et configurer des rappels pour celui-ci. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L’appel de fonction a réussi.
    
MAPI_E_NOT_FOUND
  
- L’appel de fonction a échoué.
    
## <a name="remarks"></a>Remarques

Il s’agit du premier appel qu’un client effectue lorsqu’il souhaite être averti des changements d’état de connexion pour un profil donné. Lors de **l’appel de HrOpenOfflineObj**, le client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. Le client peut vérifier les types de rappels pris en charge par l’objet (à l’aide de [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), puis configurer les rappels pour celui-ci (à l’aide [d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
Lorsque vous [utilisez GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrOpenOfflineObj@20** comme nom de procédure. 
  
 **HrOpenOfflineObj** fonctionne uniquement pour les clients qui sont des fournisseurs MAPI, des compl?ments COM et des extensions client Exchange en cours d’exécution dans le processus Outlook. Dans le cas **contraire, HrOpenOfflineObj** renvoie **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

