---
title: Fourniture de rapports de lecture et non lus pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432337"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fourniture de rapports de lecture et non lus pour les fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si un fournisseur de banque de messages peut recevoir des messages, il est nécessaire de prendre en charge les rapports de lecture et non lus des messages reçus par le fournisseur de banque de messages. Si un message reçu contient la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et que la valeur de cette propriété est true, la Banque de messages doit envoyer un message de notification à l'expéditeur lorsque l'utilisateur ouvre le message. indique que le message a été lu. De même, si l'utilisateur supprime le message avant de l'ouvrir, la Banque de messages doit émettre une réponse à l'expéditeur indiquant que le message n'a pas été lu.
  
L'émission de ces rapports est une question de création d'un objet [IMessage: IMAPIProp](imessageimapiprop.md) , de remplissage des propriétés pertinentes du message et de son envoi au SPOULEur MAPI, comme si le message était à l'origine de l'utilisateur. La méthode [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) peut être utilisée pour cela. 
  
> [!NOTE]
> Une attention particulière doit être entreprise lorsqu'une banque de messages effectue des copies d'un message non lu avec des rapports de lecture ou non lus en attente. Ces rapports ne doivent pas être générés lorsque les utilisateurs lisent les copies d'un message pour lequel des rapports ont été demandés. Lors de la copie d'un tel message, le fournisseur de banque de messages doit inclure les indicateurs CLEAR_RN_PENDING et CLEAR_NRN_PENDING dans ses appels à [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) et [IMessage:: SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

