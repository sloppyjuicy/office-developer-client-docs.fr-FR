---
title: Gestion des notifications de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 874f5954ad24c2714ba06e0050f3bb00b6ef160c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604963"
---
# <a name="handling-table-notification"></a>Gestion des notifications de la table

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Au lieu de s’inscrire directement avec un objet source de conseil, tel qu’un dossier ou un utilisateur de messagerie, un client peut s’inscrire pour les notifications dans un contenu ou une table hiérarchique. Le suivi des modifications apportées aux entrées, dossiers et messages du carnet d’adresses par le biais d’un contenu ou d’une table hiérarchique peut être plus simple et plus simple que par le biais d’objets individuels. 

Par exemple, vous pouvez appeler [IMAPITable::Advise](imapitable-advise.md) on a folder’s hierarchy table to discover when changes occur to one of its subfolders. Si vous prendre en charge l’affichage des messages distants, inscrivez-vous dans la table d’état pour observer l’activité des fournisseurs de transport et dupooler MAPI. 
  
Toutefois, il n’est pas toujours préférable d’utiliser des notifications de tableau plutôt que des notifications d’objet. La surveillance des modifications apportées au nombre de messages dans un dossier est un exemple de cas où votre client peut avoir besoin de s’inscrire aux notifications d’objet sur un dossier plutôt que sur une table implémentée par le dossier.
  

