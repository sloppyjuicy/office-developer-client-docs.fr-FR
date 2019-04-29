---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409565"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Implémente un objet de récepteur de notifications pour la gestion de la notification. Un pointeur vers un objet de récepteur Advise est transmis dans un appel à la méthode **Advise** d'un fournisseur de services, le mécanisme utilisé pour s'inscrire à la notification. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets de récepteur de notifications  <br/> |
|Implémenté par :  <br/> |Applications clientes et MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Type de pointeur:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Répond à une notification en effectuant une ou plusieurs tâches. Les tâches effectuées dépendent du type d'événement et de l'objet qui génère la notification.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

