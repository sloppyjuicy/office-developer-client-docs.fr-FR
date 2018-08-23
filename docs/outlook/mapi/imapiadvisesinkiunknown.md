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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573802"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Implémente un objet de récepteur advise pour la gestion des notifications. Un pointeur vers un objet de récepteur advise est passé à un appel à la méthode **Advise** d’un fournisseur de service, le mécanisme utilisé pour l’enregistrement d’une notification. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets de récepteur de notification  <br/> |
|Implémentée par :  <br/> |Les applications clientes et MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Répond à une notification en effectuant une ou plusieurs tâches. Les tâches exécutées varient selon le type d’événement et l’objet qui génère la notification.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

