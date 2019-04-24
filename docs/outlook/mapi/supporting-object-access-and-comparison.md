---
title: Prise en charge de l'accès aux objets et comparaison
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349608"
---
# <a name="supporting-object-access-and-comparison"></a>Prise en charge de l'accès aux objets et comparaison

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport:: OpenEntry](imapisupport-openentry.md) et [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) pour ouvrir et comparer des objets qui appartiennent à leur fournisseur ou à d'autres fournisseurs: 
  
Comme [IMAPISession:: OpenEntry](imapisession-openentry.md) pour les clients, les fournisseurs peuvent utiliser la méthode **OpenEntry** de l'objet de prise en charge pour accéder à n'importe quel objet tant qu'ils connaissent l'identificateur d'entrée de l'objet. Contrairement à la méthode session, la méthode support exige que vous spécifiez un identificateur d'entrée valide dans le paramètre _lpEntryID_ . Il ne peut pas être NULL. 
  
Pour illustrer comment un fournisseur de transport peut utiliser **IMAPISupport:: OpenEntry**, considérez le scénario suivant. Le fournisseur de transport a reçu un message au format RTF et ne sait pas si le destinataire cible peut gérer ce format. Avant de remettre le message, le fournisseur de transport doit effectuer les opérations suivantes:
  
1. Appelez la méthode [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) du message pour accéder à la table des destinataires et à l'identificateur d'entrée du destinataire, sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. TransMettez l'identificateur d'entrée à **IMAPISupport:: OpenEntry** pour ouvrir le destinataire, généralement un utilisateur de messagerie ou une liste de distribution. Le paramètre _lpInterface_ doit être défini sur null, car le fournisseur ne peut pas connaître à l'avance le type d'objet du destinataire. La méthode **OpenEntry** de l'objet support appelle [IMAPISession:: OpenEntry](imapisession-openentry.md) pour déterminer le fournisseur de carnet d'adresses responsable du destinataire. L'objet session appelle ensuite la méthode **OpenEntry** du fournisseur de carnet d'adresses approprié pour ouvrir le destinataire et renvoyer un pointeur d'interface vers le fournisseur de transport. 
    
3. Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du destinataire pour extraire sa propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Si **PR_SEND_RICH_INFO** est défini sur true, le destinataire peut gérer le texte mis en forme. 
    
Si vous avez ouvert plusieurs objets à partir d'autres fournisseurs, il se peut que vous deviez savoir si deux identificateurs d'entrée font référence au même objet. Par exemple, vous pouvez avoir un identificateur d'entrée à court terme et un identificateur d'entrée à long terme, et ces identificateurs peuvent ou non identifier le même objet. Pour éviter tout traitement redondant, appelez la méthode [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) pour comparer ces identificateurs d'entrée. Vous devez utiliser cette méthode pour la comparaison des identificateurs d'entrée, car les identificateurs d'entrée ne peuvent pas être directement comparés. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

