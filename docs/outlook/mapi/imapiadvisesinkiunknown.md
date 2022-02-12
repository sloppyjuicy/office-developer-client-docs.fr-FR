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
ms.openlocfilehash: 35b50e0ad181839744692c98ea0b4c2f267fe6b5
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773571"
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
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Répond à une notification en faisant une ou plusieurs tâches. Les tâches effectuées dépendent du type d’événement et de l’objet qui génère la notification. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

