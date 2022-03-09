---
title: Fourniture de rapports en lecture et non lus pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
ms.openlocfilehash: 06297342f9aaa7b5a4bcb878cd7c740e8fa0b3dc
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374235"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fourniture de rapports en lecture et non lus pour les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si un fournisseur de magasins de messages peut recevoir des messages, il est nécessaire de prendre en charge les rapports de lecture et les rapports non lus des messages reçus par le fournisseur de la boutique de messages. Si un message reçu contient la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et que la valeur de cette propriété est TRUE, la boutique de messages doit envoyer un message de notification à l’expéditeur lorsque l’utilisateur ouvre le message, indiquant que le message a été lu. De même, si l’utilisateur supprime le message avant de l’ouvrir, la boutique de messages doit envoyer une réponse à l’expéditeur indiquant que le message n’a pas été lu.
  
L’émission de ces rapports consiste à créer un objet [IMessage : IMAPIProp](imessageimapiprop.md) , à remplir les propriétés pertinentes du message et à l’envoyer aupooler MAPI comme si le message provenait de l’utilisateur. La [méthode IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) peut être utilisée pour cela. 
  
> [!NOTE]
> Une attention particulière doit être prise lorsqu’une magasin de messages effectue des copies d’un message non lu avec des rapports en attente de lecture ou non lus. Ces rapports ne doivent pas être générés lorsque les utilisateurs lisent des copies d’un message pour lequel des rapports ont été demandés. Lorsque vous copiez un tel message, le fournisseur de magasins de messages doit inclure les indicateurs CLEAR_RN_PENDING et CLEAR_NRN_PENDING dans ses appels à [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) et [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

