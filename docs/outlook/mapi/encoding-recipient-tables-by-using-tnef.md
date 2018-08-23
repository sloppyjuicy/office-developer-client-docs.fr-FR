---
title: Codage des tables de destinataires avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: aa2120b5d64eece76f8882489de4388b04afa053
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591344"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codage des tables de destinataires avec TNEF

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le type de codage d’un tableau de destinataire dans le flux TNEF est rarement nécessaire dans la mesure où les systèmes de messagerie plus en charge les listes de destinataires directement. En règle générale, les propriétés du destinataire sont transmises dans l’en-tête du message. Lors de l’inclusion de la table de destinataires est nécessaire, TNEF peut coder la table du destinataire dans le cadre de son traitement normal. Cette opération est effectuée pendant la phase initiale du traitement TNEF. Le fournisseur de transport peut inclure la table des destinataires du message en appelant la méthode [ITnef::AddProps](itnef-addprops.md) avec la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) spécifiée dans la liste d’inclusion. Obtient la table de destinataires du message, TNEF interroge l’ensemble de colonnes et traite chaque ligne du tableau dans le flux TNEF.
  
Une autre méthode est disponible si le fournisseur de transport a besoin de modifier la table de destinataires avant le codage. Le fournisseur de transport peut construire la table nécessaire, puis appelez la méthode [ITnef::EncodeRecips](itnef-encoderecips.md) . Si NULL est indiqué dans le paramètre _lpRecipTable_ , la table de destinataires provient directement à partir du message comme indiqué pour **ITnef::AddProps**.
  

