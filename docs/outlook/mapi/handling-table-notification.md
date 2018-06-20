---
title: Gestion de notification de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783447"
---
# <a name="handling-table-notification"></a>Gestion de notification de la table

**S’applique à**: Outlook 
  
En guise d’alternative à l’enregistrement directement avec un objet source advise, par exemple un dossier ou un utilisateur de messagerie, un client peut s’inscrire pour les notifications sur un contenu ou une table de hiérarchie. Suivi des modifications à l’adresse carnet d’entrées, dossiers et messages via un contenu ou table de hiérarchie peut être plus simple et plus simple que par le biais des objets individuels. 

Par exemple, vous pouvez appeler [IMAPITable::Advise](imapitable-advise.md) sur la table de hiérarchie d’un dossier pour découvrir les modifications sont apportées à un de ses sous-dossiers. Si vous prenez en charge l’affichage des messages à distance, enregistrez la table d’état à respecter le spouleur MAPI et l’activité par les fournisseurs de transport. 
  
Toutefois, il n’est pas toujours préférable d’utiliser des notifications de table au lieu des notifications de l’objet. Suivi des modifications dans le nombre de messages dans un dossier est un exemple de lorsque votre client peut être nécessaire d’enregistrer les notifications d’objet dans un dossier, plutôt que sur une table implémentée par le dossier.
  

