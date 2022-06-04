---
title: Threading dans MAPI
description: Décrit le thread dans MAPI, notamment la façon dont les clients MAPI utilisent des modèles de thread génériques. Cela s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
ms.openlocfilehash: f15065cac6f761d4a1f3d64808d828a195dd39c1
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894249"
---
# <a name="threading-in-mapi"></a>Threading dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un thread est l’entité de base à laquelle un système d’exploitation alloue du temps processeur. Un thread a ses propres registres, pile, priorité et stockage, mais partage un espace d’adressage et traite des ressources telles que des jetons d’accès. Les threads partagent également de la mémoire, avec un thread qui lit ce qu’un autre thread a écrit.
  
Les clients MAPI utilisent les modèles de thread génériques suivants.
  
|**Modèle de thread**|**Description**|
|:-----|:-----|
|Modèle de thread unique  <br/> |Tous les objets sont utilisés sur le thread unique. |
|Modèle de thread d’appartement  <br/> |Un objet peut être utilisé uniquement sur le thread qui l’a créé. |
|Modèle de thread gratuit, ou thread-party  <br/> |Un objet peut être utilisé sur n’importe quel thread. |
   
MAPI utilise le modèle de thread gratuit, qui prend en charge les objets thread-safe qui peuvent être utilisés sur n’importe quel thread à tout moment. OLE utilise le modèle de thread d’appartement. Le modèle de thread d’appartement prend en charge les objets qui doivent être explicitement transférés lorsqu’un thread autre que celui qui a créé l’objet doit utiliser cet objet.
  
Le mécanisme utilisé par OLE pour transférer des objets d’un thread vers un autre est appelé marshaling. Le marshaling implique un objet stub et un objet proxy. Ces objets spéciaux empaquetent les paramètres de l’interface dans l’objet à marshaler, transfèrent ces paramètres vers l’autre thread et les déballent à leur arrivée. Un conflit entre les deux modèles multithreads survient lorsqu’un objet MAPI à thread libre est envoyé à un autre processus à l’aide de l’appel de procédure distante OLE « léger » ou LRPC. LRPC modifie la sémantique de l’objet, qui passe du thread libre au threading d’appartement en interposant des interfaces de stub et de proxy avec un comportement de thread d’appartement entre l’objet et son appelant. La prise de conscience des situations dans MAPI qui entraînent ce conflit peut aider les clients et les fournisseurs de services à éviter que des problèmes ne se produisent.
  
Un objet MAPI est accessible :
  
- Par le biais d’appels directs à ses méthodes à l’aide d’un pointeur d’interface retourné par un fournisseur de services ou MAPI lié au processus du client, tel que l’objet de session retourné par [MAPILogonEx](mapilogonex.md).
    
- Par le biais d’appels indirects à ses méthodes à l’aide d’un pointeur d’interface retourné par n’importe quel fournisseur de services, tel que l’objet dossier copié à partir d’un autre dossier dans [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- Par le biais d’une fonction de rappel, telle que la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) transmise à un fournisseur de services ou à MAPI dans un appel **Conseiller** ou les méthodes qui peuvent indiquer la progression d’une longue opération. 
    

