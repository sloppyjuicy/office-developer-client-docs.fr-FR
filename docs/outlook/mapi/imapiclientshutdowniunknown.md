---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9fb372e504eaeb55861b09c4151956fb102c08f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577148"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet à un client MAPI effectuer un arrêt rapide du processus de client. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objet [IMAPISession](imapisessioniunknown.md)  <br/> |
|Implémentée par :  <br/> |Sous-système MAPI  <br/> |
|Appelée par :  <br/> |Client MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIClientShutdown  <br/> |
|Type de pointeur :  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Requêtes du sous-système MAPI pour arrêt rapide prennent en charge fournie par les fournisseurs MAPI chargés.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indique l’intention de poursuivre du client MAPI arrêté.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indique l’intention du client MAPI pour quitter le processus de client immédiatement.  <br/> |
   
## <a name="remarks"></a>Remarques

L’objectif de l’arrêt rapide consiste à autoriser un client MAPI et tout fournisseur MAPI chargé avec lequel le client MAPI a une session MAPI active pour enregistrer les données et les paramètres MAPI. Cela permet au client MAPI déconnecter toutes les références externes et quitter sans entraînant la perte de données. Un client MAPI qui doit effectuer l’arrêt rapide doit utiliser l’interface **IMAPIClientShutdown** . Le client MAPI permettre obtenir un pointeur vers cette interface en appelant la méthode IUnknown::QueryInterface sur n’importe quel objet [IMAPISession](imapisessioniunknown.md) . 
  
Un client MAPI initie toujours un arrêt rapide en appelant la méthode **IMAPIClientShutdown::QueryFastShutdown** . Le sous-système MAPI répond aux requêtes du client MAPI en vérifiant si chargés fournisseurs MAPI prennent en charge l’arrêt rapide du client. L’administrateur peut utiliser les paramètres du Registre Windows pour aider à déterminer le niveau de prise en charge de fournisseur qui est nécessaire pour les clients MAPI poursuivre l’arrêt rapide. Pour plus d’informations, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).
  
Pour procéder à l’arrêt rapide, le client appelle la méthode de **IMAPIClientShutdown::NotifyProcessShutdown** pour indiquer le sous-système MAPI l’intention d’arrêter. Le client appelle ensuite la méthode **IMAPIClientShutdown::DoFastShutdown** pour indiquer que le processus client va s’arrêter immédiatement. 
  
Pour plus d’informations sur l’arrêt rapide, voir [Vue d’ensemble rapide de l’arrêt](fast-shutdown-overview.md). Pour plus d’informations sur l’exécution de l’arrêt rapide avec succès, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

