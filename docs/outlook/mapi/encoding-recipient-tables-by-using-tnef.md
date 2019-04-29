---
title: Codage des tables de destinataires à l'aide de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417958"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codage des tables de destinataires à l'aide de TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le codage d'une table de destinataires dans le flux TNEF est rarement nécessaire dans la mesure où la plupart des systèmes de messagerie prennent en charge directement les listes de destinataires. En règle générale, les propriétés du destinataire sont transmises dans l'en-tête du message. Lorsque l'inclusion de la table de destinataires est nécessaire, TNEF peut coder la table de destinataires dans le cadre de son traitement habituel. Cette opération est réalisée lors de la phase initiale du traitement TNEF. Le fournisseur de transport peut inclure la table de destinataires du message en appelant la méthode [ITnef:: AddProps](itnef-addprops.md) avec la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) spécifiée dans la liste d'inclusion. TNEF obtient le tableau de destinataires du message, interroge le jeu de colonnes et traite chaque ligne de la table dans le flux TNEF.
  
Une autre méthode est disponible si le fournisseur de transport doit modifier la table de destinataires avant d'être codée. Le fournisseur de transport peut construire la table nécessaire, puis appeler la méthode [ITnef:: EncodeRecips](itnef-encoderecips.md) . Si la valeur NULL est transmise au paramètre _lpRecipTable_ , la table de destinataires est alors directement extraite du message comme décrit pour **ITnef:: AddProps**.
  

