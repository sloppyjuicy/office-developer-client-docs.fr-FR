---
title: HrOpenOfflineObj
description: Cet article décrit la fonction HrOpenOfflineObj et fournit la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
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
ms.openlocfilehash: 8f091050b76beced28279ee2ad26582c43edd50e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812754"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet hors connexion en fonction d’un profil donné.
  
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
  
> [in] Ce paramètre n’est pas utilisé. Il doit être 0.
    
 _pwszProfileNameIn_
  
> [in] Nom du profil pour lequel se trouve l’objet hors connexion. Il doit être exprimé en Unicode. 
    
 _pGUID_
  
> [in] Pointeur vers un GUID qui peut être utilisé pour identifier de manière unique cet objet à partir d’autres objets hors connexion. Il doit être **GUID_GlobalState**.
    
 _Conservés_
  
> [in] Ce paramètre n’est pas utilisé. Il doit être **null**.
    
 _ppOfflineObj_
  
> [out] Pointeur vers l’objet hors connexion demandé. L’appelant peut utiliser ce pointeur pour accéder à l’interface [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) afin de rechercher les rappels pris en charge par cet objet et de configurer des rappels pour celui-ci. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L’appel de fonction réussit.
    
MAPI_E_NOT_FOUND
  
- Échec de l’appel de fonction.
    
## <a name="remarks"></a>Remarques

Il s’agit du premier appel qu’un client effectue lorsqu’il souhaite être informé des modifications apportées à l’état de connexion pour un profil donné. Lors de **l’appel de HrOpenOfflineObj**, le client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. Le client peut rechercher les types de rappels pris en charge par l’objet (à l’aide [d’IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), puis configurer des rappels pour celui-ci (à l’aide [d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
Lorsque [vous utilisez GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrOpenOfflineObj@20** comme nom de procédure. 
  
 **HrOpenOfflineObj** fonctionne uniquement pour les clients qui sont des fournisseurs MAPI, des compléments COM et des extensions clientes Exchange s’exécutant dans le processus Outlook. Sinon, **HrOpenOfflineObj** retourne **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

