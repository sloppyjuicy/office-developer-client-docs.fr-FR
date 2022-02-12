---
title: Threading dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7896c2f6b3ba8007865474eb081f668ee1e16190
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781141"
---
# <a name="threading-in-mapi"></a>Threading dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un thread est l’entité de base à laquelle un système d’exploitation alloue du temps processeur. Un thread possède ses propres registres, pile, priorité et stockage, mais partage un espace d’adressaton et des ressources de processus telles que les jetons d’accès. Les threads partagent également la mémoire, avec un thread lisant ce qu’un autre thread a écrit.
  
Les clients MAPI utilisent les modèles de thread génériques suivants.
  
|**Modèle de thread**|**Description**|
|:-----|:-----|
|Modèle de thread unique  <br/> |Tous les objets sont utilisés sur le thread unique. |
|Modèle de threads de threads d’appart  <br/> |Un objet ne peut être utilisé que sur le thread qui l’a créé. |
|Modèle de thread gratuit ou de thread-party  <br/> |Un objet peut être utilisé sur n’importe quel thread. |
   
MAPI utilise le modèle de thread gratuit, qui prend en charge les objets thread-safe qui peuvent être utilisés sur n’importe quel thread à tout moment. OLE utilise le modèle de threads de threads de threads. Le modèle de threads en mode apartment prend en charge les objets qui doivent être explicitement transférés lorsqu’un thread autre que celui qui a créé l’objet doit utiliser cet objet.
  
Le mécanisme utilisé par OLE pour transférer des objets d’un thread à un autre est appelé marshaling. Le marshaling implique un objet stub et un objet proxy. Ces objets spéciaux packagent les paramètres de l’interface dans l’objet à marshaler, transfèrent ces paramètres à l’autre thread et les déballent à l’arrivée. Un conflit entre les deux modèles multithread survient lorsqu’un objet MAPI de thread libre est envoyé à un autre processus à l’aide de l’appel de procédure distante OLE « léger » ou LRPC. LRPC modifie la sémantique de l’objet de threads libres en threads de threads en threads de threads en interposant les interfaces stub et proxy avec le comportement de thread de thread entre l’objet et son appelant. La prise en compte des situations dans MAPI qui entraînent ce conflit peut aider les clients et les fournisseurs de services à éviter les problèmes.
  
Un objet MAPI est accessible :
  
- Via des appels directs à ses méthodes à l’aide d’un pointeur d’interface renvoyé par un fournisseur de services ou MAPI lié au processus du client, tel que l’objet de session renvoyé par [MAPILogonEx](mapilogonex.md).
    
- Via des appels indirects à ses méthodes à l’aide d’un pointeur d’interface renvoyé par n’importe quel fournisseur de services, tel que l’objet dossier copié à partir d’un autre dossier dans [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- Par le biais d’une fonction de rappel, telle que la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) transmise à un fournisseur de services ou  à MAPI dans un appel de conseil ou aux méthodes qui peuvent indiquer la progression d’une longue opération. 
    

