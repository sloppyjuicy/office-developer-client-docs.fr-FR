---
title: Threading dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787351"
---
# <a name="threading-in-mapi"></a>Threading dans MAPI

  
  
**S’applique à**: Outlook 
  
Un thread est l’entité de base à laquelle un système d’exploitation alloue du temps processeur. Un thread a ses propres registres, pile, priorité et stockage, mais partage un adresse espace et traiter les ressources telles que des jetons d’accès. Threads partagent également la mémoire, avec un seul thread lecture qu’un autre thread qu’il a écrite.
  
Clients MAPI utilisent les modèles de thread génériques suivantes.
  
|**Modèle de thread**|**Description**|
|:-----|:-----|
|Modèle de thread unique  <br/> |Tous les objets sont utilisés sur le thread unique.  <br/> |
|Modèle de thread Apartment  <br/> |Un objet peut être utilisé uniquement sur le thread qui l’a créé.  <br/> |
|Modèle de threading gratuite ou thread tiers  <br/> |Un objet peut être utilisé sur n’importe quel thread.  <br/> |
   
MAPI utilise le modèle de thread libre, prise en charge des objets thread-safe qui peuvent être utilisés sur n’importe quel thread à tout moment. OLE utilise le modèle de thread de cloisonnement. Le modèle de thread apartment prend en charge les objets qui doivent être transférés explicitement lorsqu’un thread différent de celui qui a créé l’objet doit utiliser cet objet.
  
Le mécanisme OLE utilise pour transférer des objets à partir d’un thread à l’autre est appelé marshaling. Le marshaling implique un objet stub et un objet proxy. Ces objets spéciaux empaqueter les paramètres de l’interface de l’objet à remarshaler, de transférer ces paramètres à l’autre thread et les décompresser à l’arrivée. Conflit entre les deux modèles multithreads se produit lorsqu’un objet MAPI libre de threads est envoyé à un autre processus utilisant OLE « léger » appel de procédure distante ou LRPC. LRPC change la sémantique de l’objet de modèle de thread libre à cloisonnement des threads par interposing interfaces stub et proxy avec apartment threading comportement entre l’objet et son appelant. Présentation des situations MAPI conduire à ce conflit peut aider les clients et fournisseurs de services éviter des problèmes.
  
Un objet MAPI est accessible :
  
- Via des appels directs à ses méthodes à l’aide d’une interface pointeur renvoyé par un fournisseur de services ou MAPI liée au processus du client, tel que l’objet session retournée à partir de [MAPILogonEx](mapilogonex.md).
    
- Par le biais des appels indirects à ses méthodes à l’aide d’un pointeur d’interface retourné par n’importe quel fournisseur de services, comme l’objet folder copiés à partir d’un autre dossier dans [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- Via une fonction de rappel, telles que la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) passée à un fournisseur de services MAPI ou un appel **Advise** ou les méthodes qui peuvent afficher la progression sur une longue opération. 
    

