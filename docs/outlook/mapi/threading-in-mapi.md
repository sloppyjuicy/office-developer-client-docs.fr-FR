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
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344827"
---
# <a name="threading-in-mapi"></a>Threading dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un thread est l'entité de base à laquelle un système d'exploitation alloue du temps processeur. Un thread a ses propres registres, pile, priorité et stockage, mais il partage un espace d'adressage et des ressources de processus telles que des jetons d'accès. Les threads partagent également la mémoire, avec un thread lisant ce qu'un autre thread a écrit.
  
Les clients MAPI utilisent les modèles de thread génériques suivants.
  
|**Modèle de thread**|**Description**|
|:-----|:-----|
|Modèle de thread unique  <br/> |Tous les objets sont utilisés sur le seul thread.  <br/> |
|Modèle de thread cloisonné  <br/> |Un objet ne peut être utilisé que sur le thread qui l'a créé.  <br/> |
|Modèle de thread libre, ou modèle de thread, modèle  <br/> |Un objet peut être utilisé sur n'importe quel thread.  <br/> |
   
MAPI utilise le modèle de thread libre, qui prend en charge les objets thread-safe qui peuvent être utilisés sur n'importe quel thread à tout moment. OLE utilise le modèle de thread cloisonné. Le modèle de thread cloisonné prend en charge les objets qui doivent être transférés explicitement lorsqu'un thread autre que celui qui a créé l'objet a besoin d'utiliser cet objet.
  
Le mécanisme utilisé par OLE pour transférer des objets d'un thread à un autre est appelé marshaling. Le marshaling implique un objet stub et un objet proxy. Ces objets spéciaux empaquetent les paramètres de l'interface dans l'objet à marshaler, transfèrent ces paramètres à l'autre thread et les décompressent lors de leur arrivée. Un conflit entre les deux modèles multithread se produit lorsqu'un objet MAPI libre de thread est envoyé à un autre processus à l'aide d'un appel de procédure disTante «léger» ou de LRPC. Les appels LRPC modifient la sémantique de l'objet de Threading libre en thread cloisonné en interposant les interfaces de proxy et de stub avec le comportement de Threading cloisonné entre l'objet et son appelant. La connaissance des situations dans MAPI qui mènent à ce conflit peut aider les clients et les fournisseurs de services à empêcher les problèmes de se produire.
  
Un objet MAPI est accessible:
  
- Par le biais d'appels directs à ses méthodes à l'aide d'un pointeur d'interface renvoyé par un fournisseur de services ou MAPI lié au processus du client, tel que l'objet session renvoyé à partir de [MAPILogonEx](mapilogonex.md).
    
- Par le biais d'appels indirects à ses méthodes à l'aide d'un pointeur d'interface retourné par un fournisseur de services, tel que l'objet Folder copié à partir d'un autre dossier dans [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md).
    
- Par le biais d'une fonction de rappel, telle que la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) transmise à un fournisseur de services ou à MAPI dans un appel de **notification** ou les méthodes qui peuvent afficher l'avancement sur une longue opération. 
    

