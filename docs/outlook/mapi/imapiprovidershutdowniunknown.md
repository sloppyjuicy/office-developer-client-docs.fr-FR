---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322405"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au sous-système MAPI d'informer un fournisseur MAPI de l'arrêt rapide d'un client MAPI, afin que le fournisseur MAPI puisse répondre à l'arrêt.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets de fournisseur: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md) <br/> |
|Implémenté par :  <br/> |Fournisseur MAPI  <br/> |
|Appelé par :  <br/> |Sous-système MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Type de pointeur:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Interroge le fournisseur MAPI pour la prise en charge de l'arrêt rapide.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indique au fournisseur MAPI qu'un client MAPI va effectuer un arrêt rapide, afin que le fournisseur puisse prendre des mesures pour empêcher toute perte de données.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indique au fournisseur MAPI que le client MAPI quitte immédiatement, afin que le fournisseur MAPI conserve les modifications afin d'éviter toute perte de données.  <br/> |
   
## <a name="remarks"></a>Remarques

L'arrêt rapide permet à un client MAPI de quitter son processus en une courte période, avec un peu de chance après que le client et les fournisseurs MAPI chargés ont enregistré les paramètres et les données MAPI. Le client MAPI lance toujours un arrêt rapide et doit interroger le sous-système MAPI pour la prise en charge de l'arrêt rapide des fournisseurs MAPI chargés. Un administrateur peut définir le Registre Windows au niveau de l'utilisateur pour spécifier le niveau de prise en charge du fournisseur nécessaire pour permettre l'arrêt rapide de tous les clients MAPI. Pour plus d'informations sur les paramètres du Registre, consultez la rubrique options de l' [utilisateur à arrêt rapide](fast-shutdown-user-options.md). Toutefois, pour que l'arrêt rapide s'exécute sans perte de données, les fournisseurs MAPI doivent implémenter l'interface **IMAPIProviderShutdown** . 
  
Un fournisseur MAPI qui doit prendre en charge l'arrêt rapide du client doit renvoyer S_OK au sous-système MAPI dans la méthode **IMAPIProviderShutdown:: QueryFastShutdown** . Lorsque le sous-système MAPI appelle ensuite les méthodes **IMAPIProviderShutdown:: NotifyProcessShutdown** et **IMAPIProviderShutdown::D ofastshutdown** , le fournisseur MAPI doit prendre les mesures nécessaires pour enregistrer les paramètres et les données MAPI et Préparez la sortie du client. 
  
Les fournisseurs MAPI qui n'ont pas besoin de prendre en charge l'arrêt rapide client doivent toujours implémenter l'interface **IMAPIProviderShutdown** et faire en sorte que la méthode **IMAPIProviderShutdown:: QueryFastShutdown** renvoie MAPI_E_NO_SUPPORT. Dans le cas d'Outlook en tant que client MAPI, Outlook attend que toutes les références externes soient libérées avant de se fermer. 
  
En fonction du paramètre de Registre Windows de l'utilisateur pour l'arrêt rapide, l'implémentation de l'interface **IMAPIProviderShutdown** n'empêche pas nécessairement un arrêt rapide du client. 
  
Pour plus d'informations sur le processus d'arrêt rapide, consultez la rubrique vue d'ensemble de l' [arrêt rapide](fast-shutdown-overview.md). Pour plus d'informations sur la façon d'effectuer l'arrêt rapide, consultez [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

