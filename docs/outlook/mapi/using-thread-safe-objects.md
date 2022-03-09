---
title: Utilisation dThread-Safe objects
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
ms.openlocfilehash: 81942f5506ab1bb8a1a90d2050d1b0ab8abae1ae
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375782"
---
# <a name="using-thread-safe-objects"></a>Utilisation dThread-Safe objects

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes peuvent supposer que les objets utilisés directement ou comme rappels sont toujours thread-safe sauf dans les cas suivants :
  
- Objet d’état d’un fournisseur de transport obtenu via un appel client à [IMAPISession::OpenEntry avec un identificateur](imapisession-openentry.md) d’entrée à partir de la ligne de table d’état du fournisseur. 
    
- Tous les objets de formulaire MAPI obtenus via un appel client [à MAPIOpenFormMgr](mapiopenformmgr.md). Les objets de formulaire respectent les règles de modèle d’appart et les clients doivent les utiliser, ainsi que tous les objets qu’ils contiennent, uniquement sur le thread qui les a créés.
    
Lorsqu’un client accède à la ligne d’un fournisseur de transport dans la table d’état qui inclut l’identificateur d’entrée de l’objet d’état associé, le client peut appeler **OpenEntry** avec cet identificateur d’entrée pour ouvrir l’objet d’état. Cet objet d’état n’est pas thread-safe, car les fournisseurs de transport s’exécutent dans le contexte dupooler MAPI et ne conservent pas de contexte distinct pour leur objet d’état. L’objet d’état respecte les règles du modèle de location et les clients doivent l’utiliser uniquement sur le thread qui l’a créé. 
  
Un client doit également appeler [MAPIInitialize](mapiinitialize.md) sur chaque thread avant d’utiliser des objets [MAPI et MAPIUninitialize](mapiuninitialize.md) lorsque cette utilisation est terminée. Ces appels doivent être effectués même si les objets à utiliser sont transmis au thread à partir d’une source externe. **MAPIInitialize** et **MAPIUninitialize** peuvent être appelés de n’importe où sauf à partir d’une fonction **DllMain** Win32, fonction appelée par le système lorsque des processus et des threads sont initialisés et terminés, ou lors d’appels aux fonctions **LoadLibrary** et **FreeLibrary** . 
  
Les objets à utilisation indirecte ne doivent jamais être supposés être thread-safe. Les objets d’utilisation indirecte sont renvoyés par des méthodes qui nécessitent des pointeurs d’interface de destination en tant que paramètres d’entrée. Par exemple, **IMAPIProp::CopyTo** et **CopyProps**, **IMAPIFolder::CopyFolder** et **CopyMessage**, et **IMsgServiceAdmin::CopyMsgService**. Si un fournisseur de services souhaite appeler un tel objet à partir d’un thread autre que celui sur lequel il a été transmis, il est responsable du marshaling explicite de l’objet.
  

