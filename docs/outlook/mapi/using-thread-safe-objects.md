---
title: À l’aide des objets Thread-Safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4a66f892043b9a90893a60f3fa6ba69ea6457f5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787469"
---
# <a name="using-thread-safe-objects"></a>À l’aide des objets Thread-Safe

  
  
**S’applique à**: Outlook 
  
Les applications clientes peuvent supposent que les objets utilisés directement ou en tant que rappels sont toujours thread-safe, sauf dans les cas suivants :
  
- Objet d’état d’un fournisseur de transport obtenu par un appel de client à [IMAPISession::OpenEntry](imapisession-openentry.md) avec un identificateur d’entrée à partir de la ligne de tableau de statut du fournisseur. 
    
- Tous les objets de formulaire MAPI obtenus par un appel de client à [MAPIOpenFormMgr](mapiopenformmgr.md). Objets de formulaire respecter les règles du modèle apartment et les clients doivent utiliser les et tous les objets contenus dans les uniquement sur le thread qui a créé les.
    
Lorsqu’un client accède à la ligne d’un fournisseur de transport dans la table d’état qui inclut l’identificateur d’entrée de l’objet associé à l’état, le client peut appeler **OpenEntry** avec cet identificateur d’entrée pour ouvrir l’objet d’état. Cet objet état n’est pas thread-safe, car les fournisseurs de transport s’exécutent dans le contexte du spouleur MAPI et ne conservent pas d’un contexte distinct pour l’objet de leur état. L’objet état se conforme aux règles du modèle apartment et clients doivent utiliser uniquement sur le thread qui l’a créé. 
  
Un client doit également appeler [exécuter MAPIInitialize](mapiinitialize.md) sur chaque thread avant d’utiliser tous les objets MAPI et [MAPIUninitialize](mapiuninitialize.md) lorsque cette utilisation est terminée. Ces appels doivent être effectuées, même si les objets utilisés sont transmis à la thread d’une source externe. **Exécuter MAPIInitialize** et **MAPIUninitialize** peuvent être appelées à partir de n’importe où à l’exception à partir d’une fonction Win32 **DllMain** , une fonction qui est appelée par le système lorsque les processus et les threads sont initialisés et arrêtés ou lors des appels vers le ** LoadLibrary** et fonctions **FreeLibrary** . 
  
Objets utilisation indirecte doivent jamais considéré comme thread-safe. Utilisation indirecte objets sont retournés par les méthodes qui nécessitent des pointeurs d’interface destination comme paramètres d’entrée. Exemples de ces méthodes sont **IMAPIProp::CopyTo** et **CopyProps**, **IMAPIFolder::CopyFolder** et **CopyMessage**et **IMsgServiceAdmin::CopyMsgService**. Si un fournisseur de services souhaite appeler ce type d’objet à partir d’un thread différent de celui sur lequel il a été passé, le fournisseur est chargé de marshaling explicite de l’objet.
  

