---
title: Tables des dossiers de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
ms.openlocfilehash: 48a8640a4a2a1a1d732dcc57443268e2d5e51678
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381396"
---
# <a name="receive-folder-tables"></a>Tables des dossiers de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de dossiers de réception contient des informations pour tous les dossiers désignés comme dossiers de réception pour une magasin de messages. Un dossier de réception est un dossier dans lequel les messages entrants d’une classe de message particulière sont placés. Les fournisseurs de magasins de messages implémentent les tables de dossiers de réception et les applications clientes les utilisent en appelant la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Les propriétés suivantes définissent le jeu de colonnes requis dans les tables des dossiers de réception :
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

