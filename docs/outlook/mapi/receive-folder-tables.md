---
title: Tables de dossiers de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417349"
---
# <a name="receive-folder-tables"></a>Tables de dossiers de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de dossiers de réception contient des informations pour tous les dossiers désignés comme dossiers de réception pour une banque de messages. Un dossier de réception est un dossier où les messages entrants d'une classe de message particulière sont placés. Les fournisseurs de banque de messages implémentent les tables de dossiers de réception et les applications clientes les utilisent en appelant la méthode [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Les propriétés suivantes constituent le jeu de colonnes requis dans les tables de dossiers de réception:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

