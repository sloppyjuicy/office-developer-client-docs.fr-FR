---
title: Fourniture de lecture et des rapports de suppression du mode lecture pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786984"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fourniture de lecture et des rapports de suppression du mode lecture pour les fournisseurs de banque de messages

  
  
**S’applique à**: Outlook 
  
Si un fournisseur de magasin de message peut recevoir des messages, il est requis pour prendre en charge la lecture des rapports et nonread de messages reçus par le fournisseur de banque de messages. Si un message reçu contient la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et la valeur de cette propriété a la valeur TRUE, la banque de messages doit envoyer un message de notification à l’expéditeur lorsque l’utilisateur ouvre le message, indiquant que le message a été lu. De même, si l’utilisateur supprime le message avant de l’ouvrir, la banque de messages doit émettre une réponse à l’expéditeur indiquant que le message n’a pas été lu.
  
Émission de ces rapports est une question de la création d’un [IMessage : IMAPIProp](imessageimapiprop.md) objet, remplissez les propriétés pertinentes sur le message et l’envoi au spouleur MAPI comme si le message avait à l’origine de l’utilisateur. La méthode [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) peut être utilisée pour cela. 
  
> [!NOTE]
> Une attention particulière doit être prise lors d’une banque de messages effectue des copies d’un message non lu avec en attente de rapports de lecture ou nonread. Ces rapports ne doivent pas être générées lorsque les utilisateurs lire toutes les copies d’un message pour lequel les rapports ont été demandées. Lorsque vous effectuez une copie de ce message, le fournisseur de banque de messages doit inclure les indicateurs CLEAR_RN_PENDING et CLEAR_NRN_PENDING dans ses appels [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) et [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

