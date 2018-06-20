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
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783950"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**S’applique à**: Outlook 
  
Permet le sous-système MAPI informer un fournisseur MAPI de l’arrêt rapide d’un client MAPI, afin que le fournisseur MAPI peut répondre à l’arrêt.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets du fournisseur : [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md) <br/> |
|Implémentée par :  <br/> |Fournisseur MAPI  <br/> |
|Appelée par :  <br/> |Sous-système MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Requêtes le fournisseur MAPI pour arrêt rapide prennent en charge.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indique au fournisseur MAPI qu’un client MAPI sur le point d’effectuer un arrêt rapide, afin que le fournisseur peut prendre des mesures pour éviter toute perte de données.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indique au fournisseur MAPI que le client MAPI va s’arrêter immédiatement, afin que le fournisseur MAPI maintient les modifications pour éviter toute perte de données.  <br/> |
   
## <a name="remarks"></a>Remarques

Arrêt rapide permet à un client MAPI quitter son processus au sein d’un court instant, j’espère que lorsque le client et le chargement fournisseurs MAPI ont enregistré données et paramètres MAPI. Le client MAPI toujours initie un arrêt rapide et doit interroger le sous-système MAPI pour la prise en charge de l’arrêt rapide des fournisseurs MAPI chargés. Un administrateur peut définir le Registre Windows au niveau de l’utilisateur de spécifier le niveau de prise en charge de fournisseur qui est nécessaire pour permettre l’arrêt rapide de tous les clients MAPI. Pour plus d’informations sur les paramètres de Registre, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md). Toutefois, pour l’arrêt rapide se produise correctement sans perte de données, fournisseurs MAPI doivent implémenter l’interface **IMAPIProviderShutdown** . 
  
Un fournisseur MAPI qui doit prendre en charge l’arrêt rapide client doit renvoyer S_OK au sous-système MAPI dans la méthode **IMAPIProviderShutdown::QueryFastShutdown** . Lorsque le sous-système MAPI appelle ensuite les méthodes **IMAPIProviderShutdown::NotifyProcessShutdown** et **IMAPIProviderShutdown::DoFastShutdown** , le fournisseur MAPI doit prendre des mesures nécessaires pour enregistrer les données et les paramètres MAPI et Préparez la sortie du client. 
  
Fournisseurs MAPI qui n’ont pas besoin pour prendre en charge l’arrêt rapide client doivent toujours implémenter l’interface **IMAPIProviderShutdown** et que la méthode de **IMAPIProviderShutdown::QueryFastShutdown** renvoie MAPI_E_NO_SUPPORT. Pour Outlook en tant qu’un client MAPI, cela entraîne à attendre que toutes les références externes doit être publié avant de quitter Outlook. 
  
Dans le Registre Windows de l’utilisateur en fonction de paramètre d’arrêt rapide, ne pas l’implémentation de l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client. 
  
Pour plus d’informations sur le processus d’arrêt rapide, voir [Vue d’ensemble rapide de l’arrêt](fast-shutdown-overview.md). Pour plus d’informations sur la façon d’effectuer correctement arrêt rapide, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

