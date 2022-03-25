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
ms.openlocfilehash: 103c326d24e833dbdbdb91154d5f1f379dc7a019
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720233"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un client MAPI d’effectuer un arrêt rapide du processus client. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |[Objet IMAPISession](imapisessioniunknown.md)  <br/> |
|Implémenté par :  <br/> |Sous-système MAPI  <br/> |
|Appelé par :  <br/> |Client MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIClientShutdown  <br/> |
|Type de pointeur :  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Interroge le sous-système MAPI pour obtenir la prise en charge de l’arrêt rapide fourni par les fournisseurs MAPI chargés. |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indique l’intention du client MAPI de poursuivre l’arrêt. |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indique l’intention du client MAPI de quitter immédiatement le processus client. |
   
## <a name="remarks"></a>Remarques

L’objectif de l’arrêt rapide est d’autoriser un client MAPI et tout fournisseur MAPI chargé avec lequel le client MAPI dispose d’une session MAPI active à enregistrer les paramètres et les données MAPI. Cela permet au client MAPI de déconnecter toutes les références externes et de quitter sans entraîner de perte de données. Un client MAPI qui doit effectuer un arrêt rapide doit utiliser l’interface **IMAPIClientShutdown** . Le client MAPI peut obtenir un pointeur vers cette interface en appelant la méthode IUnknown::QueryInterface sur n’importe quel objet [IMAPISession](imapisessioniunknown.md) . 
  
Un client MAPI lance toujours un arrêt rapide en appelant la méthode **IMAPIClientShutdown::QueryFastShutdown** . Le sous-système MAPI répond à la requête du client MAPI en vérifiant si les fournisseurs MAPI chargés peuvent prendre en charge l’arrêt rapide du client. L’administrateur peut utiliser Windows de Registre pour déterminer le niveau de prise en charge du fournisseur nécessaire pour que les clients MAPI procèdent à un arrêt rapide. Pour plus d’informations, voir [Options utilisateur d’arrêt rapide](fast-shutdown-user-options.md).
  
Pour procéder à un arrêt rapide, le client appelle la méthode **IMAPIClientShutdown::NotifyProcessShutdown** pour indiquer au sous-système MAPI l’intention de s’arrêter. Le client appelle ensuite la méthode **IMAPIClientShutdown::D oFastShutdown** pour indiquer que le processus client se quitte immédiatement. 
  
Pour plus d’informations sur l’arrêt rapide, voir [Vue d’ensemble de l’arrêt rapide](fast-shutdown-overview.md). Pour plus d’informations sur la façon d’effectuer un arrêt rapide, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

