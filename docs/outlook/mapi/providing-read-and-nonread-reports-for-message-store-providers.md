---
title: Fourniture de rapports de lecture et non lus pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 15a2868519e5b8a4363e23ccf1cc3037d630f162
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599157"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fourniture de rapports de lecture et non lus pour les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si un fournisseur de magasins de messages peut recevoir des messages, il est nécessaire de prendre en charge les rapports de lecture et les rapports non lus des messages reçus par le fournisseur de la boutique de messages. Si un message reçu contient la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et que la valeur de cette propriété est TRUE, la boutique de messages doit envoyer un message de notification à l’expéditeur lorsque l’utilisateur ouvre le message, indiquant que le message a été lu. De même, si l’utilisateur supprime le message avant de l’ouvrir, la boutique de messages doit envoyer une réponse à l’expéditeur indiquant que le message n’a pas été lu.
  
L’émission de ces rapports consiste à créer un objet [IMessage : IMAPIProp,](imessageimapiprop.md) à remplir les propriétés pertinentes sur le message et à l’envoyer aupooler MAPI comme si le message provenait de l’utilisateur. La [méthode IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) peut être utilisée pour cela. 
  
> [!NOTE]
> Une attention particulière doit être prise lorsqu’une magasin de messages effectue des copies d’un message non lu avec des rapports en attente de lecture ou non lus. Ces rapports ne doivent pas être générés lorsque les utilisateurs lisent des copies d’un message pour lequel des rapports ont été demandés. Lors de la copie d’un tel message, le fournisseur de magasins de messages doit inclure les indicateurs CLEAR_RN_PENDING et CLEAR_NRN_PENDING dans ses appels à [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) et [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

