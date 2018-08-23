---
title: Banques de messages par d�faut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576910"
---
# <a name="default-message-stores"></a>Banques de messages par d�faut

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une banque de messages par d�faut est celle dont les applications clientes peuvent utiliser pour les t�ches de messagerie � usage g�n�ral. Il existe un certain nombre de fonctionnalit�s facultatives pour les fournisseurs de banque de message qui deviennent obligatoires si le fournisseur de banque de messages doit �tre utilis� en tant que la banque de messages par d�faut. Ils sont les suivants :
  
- Impl�mentation de dossiers sp�ciaux : les dossiers bo�te de r�ception, bo�te d'envoi et r�sultats de recherche.
    
- Fournir des rapports de lecture et nonread.
    
- Autoriser les envois de messages entrants et sortants.
    
- Autoriser la cr�ation de messages avec des classes de message arbitraires.
    
- Prise en charge des propri�t�s nomm�es et plusieurs valeurs.
    
- Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider. 
    
- Supporting associated contents tables. For more information, see [Tables des mati�res](contents-tables.md).
    
- Prise en charge des notifications de spouleur MAPI lorsqu'il existe des messages dans la file d'attente de messages sortants.
    
## <a name="see-also"></a>Voir aussi



[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

