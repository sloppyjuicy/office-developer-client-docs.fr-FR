---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: Permet au sous-système MAPI d’informer un fournisseur MAPI de l’arrêt rapide d’un client MAPI, afin que le fournisseur MAPI puisse répondre à l’arrêt.
ms.openlocfilehash: 2c37d1289a2239ab9aaab2f13582b444a7514bdb
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764334"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au sous-système MAPI d’informer un fournisseur MAPI de l’arrêt rapide d’un client MAPI, afin que le fournisseur MAPI puisse répondre à l’arrêt.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets fournisseur : [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md) ou [IMSProvider](imsprovideriunknown.md) <br/> |
|Implémenté par :  <br/> |Fournisseur MAPI  <br/> |
|Appelé par :  <br/> |Sous-système MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Propriété |Valeur |
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Interroge le fournisseur MAPI pour obtenir une prise en charge de l’arrêt rapide. |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indique au fournisseur MAPI qu’un client MAPI va faire un arrêt rapide, afin que le fournisseur puisse prendre des mesures pour empêcher la perte de données. |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indique au fournisseur MAPI que le client MAPI quitte immédiatement, afin que le fournisseur MAPI continue à apporter des modifications afin d’éviter toute perte de données. |
   
## <a name="remarks"></a>Remarques

L’arrêt rapide permet à un client MAPI de quitter son processus dans un court délai, avec un peu de chance une fois que le client et les fournisseurs MAPI chargés ont enregistré les paramètres et les données MAPI. Le client MAPI lance toujours un arrêt rapide et doit interroger le sous-système MAPI pour obtenir la prise en charge de l’arrêt rapide des fournisseurs MAPI chargés. Un administrateur peut définir le Registre Windows au niveau de l’utilisateur pour spécifier le niveau de prise en charge du fournisseur nécessaire pour autoriser l’arrêt rapide de tous les clients MAPI. Pour plus d’informations sur les paramètres du Registre, voir [Options utilisateur](fast-shutdown-user-options.md) d’arrêt rapide. Toutefois, pour que l’arrêt rapide se produise sans perte de données, les fournisseurs MAPI doivent implémenter l’interface **IMAPIProviderShutdown** . 
  
Un fournisseur MAPI qui doit prendre en charge l’arrêt rapide du client doit retourner S_OK au sous-système MAPI dans la méthode **IMAPIProviderShutdown::QueryFastShutdown** . Lorsque le sous-système MAPI appelle par la suite les méthodes **IMAPIProviderShutdown::NotifyProcessShutdown** et **IMAPIProviderShutdown::D oFastShutdown** , le fournisseur MAPI doit prendre les mesures nécessaires pour enregistrer les données et paramètres MAPI et préparer la sortie du client. 
  
Les fournisseurs MAPI qui n’ont pas besoin de prendre en charge l’arrêt rapide du client doivent toujours implémenter l’interface **IMAPIProviderShutdown** et faire en retour la méthode **IMAPIProviderShutdown::QueryFastShutdown** MAPI_E_NO_SUPPORT. Pour Outlook client MAPI, cela entraîne Outlook attendre que toutes les références externes soient libérées avant de se quitter. 
  
Selon le paramètre de Registre Windows de l’utilisateur pour l’arrêt rapide, le fait de ne pas implémenter l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client. 
  
Pour plus d’informations sur le processus d’arrêt rapide, voir [Vue d’ensemble de l’arrêt rapide](fast-shutdown-overview.md). Pour plus d’informations sur la réalisation d’un arrêt rapide, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

