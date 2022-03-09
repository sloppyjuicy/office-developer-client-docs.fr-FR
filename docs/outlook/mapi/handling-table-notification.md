---
title: Gestion des notifications de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
ms.openlocfilehash: 6737296794f6463b3d5b8dd58d1fa5bc8c6ba076
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372961"
---
# <a name="handling-table-notification"></a>Gestion des notifications de la table

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Au lieu de s’inscrire directement avec un objet source de conseil, tel qu’un dossier ou un utilisateur de messagerie, un client peut s’inscrire pour les notifications dans un contenu ou une table hiérarchique. Le suivi des modifications apportées aux entrées, dossiers et messages du carnet d’adresses par le biais d’un contenu ou d’une table hiérarchique peut être plus simple et plus simple que par le biais d’objets individuels. 

Par exemple, vous pouvez appeler [IMAPITable::Advise](imapitable-advise.md) on a folder’s hierarchy table to discover when changes occur to one of its subfolders. Si vous prendre en charge l’affichage des messages distants, inscrivez-vous dans la table d’état pour observer l’activité des fournisseurs de transport et dupooler MAPI. 
  
Toutefois, il n’est pas toujours préférable d’utiliser des notifications de tableau plutôt que des notifications d’objet. La surveillance des modifications apportées au nombre de messages dans un dossier est un exemple de cas où votre client peut avoir besoin de s’inscrire aux notifications d’objet sur un dossier plutôt que sur une table implémentée par le dossier.
  

