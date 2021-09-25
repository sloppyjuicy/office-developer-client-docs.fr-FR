---
title: Prise en charge de l’accès et de la comparaison des objets
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9383cd11a9183032d2aeaa7621b72592700e977c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609472"
---
# <a name="supporting-object-access-and-comparison"></a>Prise en charge de l’accès et de la comparaison des objets

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport::OpenEntry](imapisupport-openentry.md) et [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) pour ouvrir et comparer des objets appartenant à leur fournisseur ou à d’autres fournisseurs : 
  
Comme [IMAPISession::OpenEntry](imapisession-openentry.md) pour les clients, les fournisseurs peuvent utiliser la méthode **OpenEntry** de leur objet de support pour accéder à n’importe quel objet tant qu’ils connaissent l’identificateur d’entrée de l’objet. Contrairement à la méthode de session, la méthode de prise en charge nécessite de spécifier un identificateur d’entrée valide dans le paramètre _lpEntryID._ Elle ne peut pas être NULL. 
  
Pour illustrer comment un fournisseur de transport peut utiliser **IMAPISupport::OpenEntry,** envisagez le scénario suivant. Le fournisseur de transport a reçu un message mis en forme au format Texte enrichi et ne sait pas si le destinataire cible peut gérer ce format. Avant de remettre le message, le fournisseur de transport doit :
  
1. Appelez la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message pour accéder à la table des destinataires et à l’identificateur d’entrée du destinataire, sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Passez l’identificateur d’entrée à **IMAPISupport::OpenEntry** pour ouvrir le destinataire, généralement un utilisateur de messagerie ou une liste de distribution. Le  _paramètre lpInterface_ doit avoir la valeur NULL, car le fournisseur ne peut pas connaître à l’avance le type d’objet du destinataire. La méthode **OpenEntry** de l’objet de support appelle [IMAPISession::OpenEntry](imapisession-openentry.md) pour déterminer le fournisseur de carnet d’adresses responsable du destinataire. L’objet de session appelle ensuite la méthode **OpenEntry** du fournisseur de carnet d’adresses approprié pour ouvrir le destinataire et renvoyer un pointeur d’interface vers le fournisseur de transport. 
    
3. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du destinataire pour récupérer sa propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Si **PR_SEND_RICH_INFO** est définie sur TRUE, le destinataire peut gérer le texte mis en forme. 
    
Si vous avez ouvert plusieurs objets à partir d’autres fournisseurs, vous devrez peut-être déterminer si deux identificateurs d’entrée font référence au même objet. Par exemple, vous pouvez avoir un identificateur d’entrée à court terme et un identificateur d’entrée à long terme, et ces identificateurs peuvent ou non identifier le même objet. Pour éviter un traitement redondant, appelez la méthode [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) pour comparer ces identificateurs d’entrée. Vous devez utiliser cette méthode pour la comparaison des identificateurs d’entrée, car les identificateurs d’entrée ne peuvent pas être comparés directement. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

