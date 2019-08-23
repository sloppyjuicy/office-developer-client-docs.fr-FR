---
title: Banques de messages par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338044"
---
# <a name="default-message-stores"></a>Banques de messages par défaut

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une banque de messages par défaut est une banque de messages pouvant être utilisée par les applications clientes pour des tâches de messagerie à usage général. Certaines fonctionnalités facultatives pour les fournisseurs de banques de messages deviennent nécessaires si le fournisseur de banques de messages doit être utilisé en tant que banque de messages par défaut. Ces fonctionnalités sont les suivantes :
  
- Implémentation des dossiers spéciaux : les dossiers Boîte de réception, Boîte d’envoi et résultats de recherche.
    
- Fournir des rapports de lecture et nonread.
    
- Autoriser les envois de messages entrants et sortants.
    
- Autorisation de la création de messages avec classes de messages arbitraires.
    
- Prise en charge des propriétés nommées et à valeurs multiples.
    
- Prise en charge de la méthode [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), même si le fournisseur de banques de messages est étroitement associé à un fournisseur de transport. 
    
- Prise en charge des tables des matières associées. Pour plus d’informations, reportez-vous à [Tables des matières](contents-tables.md).
    
- Prise en charge des notifications de spouleur MAPI lorsqu'il existe des messages dans la file d'attente de messages sortants.
    
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

