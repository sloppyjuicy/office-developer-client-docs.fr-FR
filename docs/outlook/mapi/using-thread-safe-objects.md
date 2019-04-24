---
title: Utilisation d'objets thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329588"
---
# <a name="using-thread-safe-objects"></a>Utilisation d'objets thread-safe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes peuvent supposer que les objets utilisés directement ou en tant que rappels sont toujours thread-safe, sauf dans les cas suivants:
  
- Objet d'état d'un fournisseur de transport obtenu via un appel client vers [IMAPISession:: OpenEntry](imapisession-openentry.md) avec un identificateur d'entrée de la ligne de la table d'État du fournisseur. 
    
- Tous les objets de formulaire MAPI obtenus par le biais d'un appel client vers [MAPIOpenFormMgr](mapiopenformmgr.md). Les objets Form obéissent aux règles de modèle cloisonné et les clients doivent les utiliser et tous les objets qu'ils contiennent uniquement sur le thread qui les a créés.
    
Lorsqu'un client accède à la ligne d'un fournisseur de transport dans la table d'État qui contient l'identificateur d'entrée de l'objet d'état associé, le client peut appeler **OpenEntry** avec cet identificateur d'entrée pour ouvrir l'objet d'État. Cet objet Status n'est pas thread-safe car les fournisseurs de transport s'exécutent dans le contexte du spouleur MAPI et ne gèrent pas de contexte distinct pour leur objet d'État. L'objet Status obéit aux règles de modèle cloisonné et les clients ne doivent l'utiliser que sur le thread qui l'a créé. 
  
Un client doit également appeler [MAPIInitialize](mapiinitialize.md) sur chaque thread avant d'utiliser les objets MAPI et [MAPIUninitialize](mapiuninitialize.md) lorsque cette utilisation est terminée. Ces appels doivent être effectués même si les objets à utiliser sont transmis au thread à partir d'une source externe. **MAPIInitialize** et **MAPIUninitialize** peuvent être appelés depuis n'importe quel endroit, sauf à partir d'une fonction **DllMain** Win32, d'une fonction appelée par le système lorsque les processus et les **threads sont initialisés et terminés, ou lorsque des appels au Fonctions LoadLibrary** et **FreeLibrary** . 
  
Les objets d'utilisation inDirecte ne doivent jamais être considérés comme thread-safe. Les objets use inDirects sont renvoyés par les méthodes qui nécessitent des pointeurs d'interface de destination comme paramètres d'entrée. Les exemples de ces méthodes sont **IMAPIProp:: CopyTo** et **CopyProps**, **IMAPIFolder:: CopyFolder** et **CopyMessage**, et **IMsgServiceAdmin:: CopyMsgService**. Si un fournisseur de services souhaite appeler ce type d'objet à partir d'un autre thread que celui sur lequel il a été passé, le fournisseur est chargé de marshaler explicitement l'objet.
  

