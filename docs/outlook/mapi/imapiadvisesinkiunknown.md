---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1807497f75b37b4aed041ba680cdd231337157e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600952"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Implémente un objet de réception de notification pour la gestion des notifications. Un pointeur vers un objet de réception de notification est transmis dans un appel à la méthode **Advise** d’un fournisseur de services, le mécanisme utilisé pour s’inscrire pour la notification. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Conseiller les objets de sink  <br/> |
|Implémenté par :  <br/> |Applications clientes et MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Répond à une notification en effectuent une ou plusieurs tâches. Les tâches effectuées dépendent du type d’événement et de l’objet qui génère la notification.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

