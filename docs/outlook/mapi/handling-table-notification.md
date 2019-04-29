---
title: Gestion des notifications de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435893"
---
# <a name="handling-table-notification"></a>Gestion des notifications de la table

**S’applique à** : Outlook 2013 | Outlook 2016 
  
En guise d'alternative à l'inscription directe avec un objet de source de notification, tel qu'un dossier ou un utilisateur de messagerie, un client peut s'inscrire pour des notifications sur une table des matières ou une table de hiérarchie. Le suivi des modifications apportées aux entrées de carnet d'adresses, aux dossiers et aux messages via un tableau de contenu ou de hiérarchie peut être plus simple et plus simple qu'avec des objets individuels. 

Par exemple, vous pouvez appeler la fonction [IMAPITable:: Advise](imapitable-advise.md) sur la table de hiérarchie d'un dossier pour détecter les modifications apportées à l'un de ses sous-dossiers. Si vous prenez en charge l'affichage des messages distants, inscrivez-vous à l'aide de la table d'État pour observer l'activité par les fournisseurs de transport et le spouleur MAPI. 
  
Toutefois, il n'est pas toujours préférable d'utiliser des notifications de table au lieu de notifications d'objet. Le suivi des modifications apportées au nombre de messages dans un dossier est un exemple de la nécessité pour votre client d'inscrire des notifications d'objet sur un dossier plutôt que sur une table implémentée par le dossier.
  

