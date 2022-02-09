---
title: Codage des tables des destinataires à l’aide du TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 043101e89c59d44b148b542e39b476c6c661098e
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461868"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codage des tables des destinataires à l’aide du TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le codage d’une table des destinataires dans le flux TNEF est rarement nécessaire, car la plupart des systèmes de messagerie prendre en charge les listes de destinataires directement. En règle générale, les propriétés du destinataire sont transmises dans l’en-tête du message. Lorsque l’inclusion de la table des destinataires est nécessaire, le TNEF peut encoder la table des destinataires dans le cadre de son traitement habituel. Cette étape est effectuée lors de la phase initiale du traitement TNEF. Le fournisseur de transport peut inclure la table des destinataires du message en appelant la méthode [ITnef::AddProps](itnef-addprops.md) avec la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) spécifiée dans la liste d’inclusion. TNEF obtient la table des destinataires à partir du message, interroge le jeu de colonnes et traite chaque ligne de la table dans le flux TNEF.
  
Une autre méthode est disponible si le fournisseur de transport doit modifier la table des destinataires avant qu’elle ne soit codée. Le fournisseur de transport peut construire la table nécessaire, puis appeler la méthode [ITnef::EncodeRecips](itnef-encoderecips.md) . Si NULL est transmis dans le paramètre _lpRecipTable_ , la table des destinataires est directement tirée du message comme décrit pour **ITnef::AddProps**.
  

