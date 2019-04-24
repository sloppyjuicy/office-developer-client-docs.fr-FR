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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350875"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un client MAPI de procéder à l'arrêt rapide du processus client. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objet [IMAPISession](imapisessioniunknown.md)  <br/> |
|Implémenté par :  <br/> |Sous-système MAPI  <br/> |
|Appelé par :  <br/> |Client MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Type de pointeur:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Interroge le sous-système MAPI pour la prise en charge de l'arrêt rapide fourni par les fournisseurs MAPI chargés.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indique l'intention du client MAPI de continuer à arrêter.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indique l'intention du client MAPI de quitter immédiatement le processus client.  <br/> |
   
## <a name="remarks"></a>Remarques

L'objectif de l'arrêt rapide est de permettre à un client MAPI et à tout fournisseur MAPI chargé avec lequel le client MAPI dispose d'une session MAPI active pour enregistrer les paramètres et les données MAPI. Cela permet au client MAPI de déconnecter toutes les références externes et de quitter sans provoquer de perte de données. Un client MAPI qui doit effectuer un arrêt rapide doit utiliser l'interface **IMAPIClientShutdown** . Le client MAPI peut obtenir un pointeur vers cette interface en appelant la méthode IUnknown:: QueryInterface sur n'importe quel objet [IMAPISession](imapisessioniunknown.md) . 
  
Un client MAPI lance toujours un arrêt rapide en appelant la méthode **IMAPIClientShutdown:: QueryFastShutdown** . Le sous-système MAPI répond à la requête du client MAPI en vérifiant si les fournisseurs MAPI chargés prennent en charge l'arrêt rapide du client. L'administrateur peut utiliser les paramètres du Registre Windows pour déterminer le niveau de prise en charge des fournisseurs qui est nécessaire pour permettre aux clients MAPI de poursuivre l'arrêt rapide. Pour plus d'informations, consultez la rubrique options de l' [utilisateur à arrêt rapide](fast-shutdown-user-options.md).
  
Pour poursuivre l'arrêt rapide, le client appelle la méthode **IMAPIClientShutdown:: NotifyProcessShutdown** pour indiquer au sous-système MAPI l'intention de s'arrêter. Le client appelle ensuite la méthode **IMAPIClientShutdown::D ofastshutdown** pour indiquer que le processus client quitte immédiatement. 
  
Pour plus d'informations sur l'arrêt rapide, consultez la rubrique [vue d'ensemble de l'arrêt rapide](fast-shutdown-overview.md). Pour plus d'informations sur la façon d'effectuer l'arrêt rapide, consultez [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)
  
[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)

