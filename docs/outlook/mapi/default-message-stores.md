---
title: Banques de messages par d�faut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
ms.openlocfilehash: 25d648d667273d53cdb4ee18546f15527e384d17
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370462"
---
# <a name="default-message-stores"></a>Banques de messages par défaut

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une banque de messages par défaut est une banque de messages pouvant être utilisée par les applications clientes pour des tâches de messagerie à usage général. Certaines fonctionnalités facultatives pour les fournisseurs de banques de messages deviennent nécessaires si le fournisseur de banques de messages doit être utilisé en tant que banque de messages par défaut. Ces fonctionnalités sont les suivantes :
  
- Impl�mentation de dossiers sp�ciaux : les dossiers bo�te de r�ception, bo�te d'envoi et r�sultats de recherche.
    
- Fournir des rapports de lecture et nonread.
    
- Autoriser les envois de messages entrants et sortants.
    
- Autoriser la cr�ation de messages avec des classes de message arbitraires.
    
- Prise en charge des propri�t�s nomm�es et plusieurs valeurs.
    
- Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider. 
    
- Supporting associated contents tables. For more information, see [Tables des mati�res](contents-tables.md).
    
- Prise en charge des notifications de spouleur MAPI lorsqu'il existe des messages dans la file d'attente de messages sortants.
    
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

