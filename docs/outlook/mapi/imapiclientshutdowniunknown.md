---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8243ab5a342c402946812a61ca199af0d17803b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567612"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un client MAPI d’effectuer un arrêt rapide du processus client. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |[Objet IMAPISession](imapisessioniunknown.md)  <br/> |
|Implémenté par :  <br/> |Sous-système MAPI  <br/> |
|Appelé par :  <br/> |Client MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIClientShutdown  <br/> |
|Type de pointeur :  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Interroge le sous-système MAPI pour obtenir la prise en charge de l’arrêt rapide fourni par les fournisseurs MAPI chargés.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indique l’intention du client MAPI de poursuivre l’arrêt.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indique l’intention du client MAPI de quitter immédiatement le processus client.  <br/> |
   
## <a name="remarks"></a>Remarques

L’objectif d’un arrêt rapide est d’autoriser un client MAPI et tout fournisseur MAPI chargé avec lequel le client MAPI dispose d’une session MAPI active à enregistrer les paramètres et les données MAPI. Cela permet au client MAPI de déconnecter toutes les références externes et de quitter sans entraîner de perte de données. Un client MAPI qui doit effectuer un arrêt rapide doit utiliser l’interface **IMAPIClientShutdown.** Le client MAPI peut obtenir un pointeur vers cette interface en appelant la méthode IUnknown::QueryInterface sur n’importe quel objet [IMAPISession.](imapisessioniunknown.md) 
  
Un client MAPI lance toujours un arrêt rapide en appelant la méthode **IMAPIClientShutdown::QueryFastShutdown.** Le sous-système MAPI répond à la requête du client MAPI en vérifiant si les fournisseurs MAPI chargés peuvent prendre en charge l’arrêt rapide du client. L’administrateur peut utiliser Windows de Registre pour déterminer le niveau de prise en charge du fournisseur nécessaire pour que les clients MAPI procèdent à un arrêt rapide. Pour plus d’informations, voir [Options utilisateur d’arrêt rapide.](fast-shutdown-user-options.md)
  
Pour procéder à un arrêt rapide, le client appelle la méthode **IMAPIClientShutdown::NotifyProcessShutdown** pour indiquer au sous-système MAPI l’intention de s’arrêter. Le client appelle ensuite la méthode **IMAPIClientShutdown::D oFastShutdown** pour indiquer que le processus client se quitte immédiatement. 
  
Pour plus d’informations sur l’arrêt rapide, voir [Vue d’ensemble de l’arrêt rapide.](fast-shutdown-overview.md) Pour plus d’informations sur la façon d’effectuer un arrêt rapide, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

