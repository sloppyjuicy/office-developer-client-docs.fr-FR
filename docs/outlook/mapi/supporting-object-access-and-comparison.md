---
title: Prise en charge l’accès aux objets et comparaison
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2152cfbb91f2e343ebcee3f5b717a29805df1d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787315"
---
# <a name="supporting-object-access-and-comparison"></a>Prise en charge l’accès aux objets et comparaison

  
  
**S’applique à**: Outlook 
  
Fournisseurs de services peuvent utiliser les méthodes [IMAPISupport::OpenEntry](imapisupport-openentry.md) et [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) pour ouvrir et comparer les objets qui appartiennent à leur fournisseur ou à d’autres fournisseurs : 
  
Comme [IMAPISession::OpenEntry](imapisession-openentry.md) pour les clients, fournisseurs peuvent utiliser la méthode **OpenEntry** de l’objet de leur prise en charge pour accéder à n’importe quel objet comme ils connaissent l’identificateur d’entrée de l’objet. Contrairement à la méthode de session, la méthode de prise en charge nécessite que vous spécifiez un identificateur d’entrée valide dans le paramètre _lpEntryID_ . Il ne peut pas être NULL. 
  
Pour illustrer comment un fournisseur de transport peut utiliser **IMAPISupport::OpenEntry**, examinez le scénario suivant. Le fournisseur de transport a reçu un message mis en forme au Format RTF et ne sait pas si le destinataire cible peut gérer ce format. Avant de remettre le message, le fournisseur de transport doit effectuer les opérations suivantes :
  
1. Appelez la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message pour accéder à la table de destinataires et l’identificateur d’entrée du destinataire, sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Passez l’identificateur d’entrée pour **IMAPISupport::OpenEntry** pour ouvrir le destinataire, généralement soit une messagerie utilisateur ou liste de distribution. Le paramètre _lpInterface_ doit être défini sur NULL car le fournisseur ne peut pas savoir à l’avance le type d’objet du destinataire. La prise en charge de méthode l’objet **OpenEntry** appelle [IMAPISession::OpenEntry](imapisession-openentry.md) pour déterminer le fournisseur de carnet d’adresses responsable du destinataire. L’objet session appelle ensuite la méthode de **OpenEntry** du fournisseur livre adresse appropriée pour ouvrir le destinataire et retourne un pointeur d’interface pour le fournisseur de transport. 
    
3. Appelez [IMAPIProp::GetProps](imapiprop-getprops.md) méthode le destinataire pour récupérer sa propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Si **PR_SEND_RICH_INFO** est défini sur TRUE, le destinataire peut gérer le texte mis en forme. 
    
Si vous avez ouvert plusieurs objets à partir d’autres fournisseurs, vous devrez peut-être savoir si les deux identificateurs d’entrée font référence au même objet. Par exemple, vous devrez peut-être un identificateur d’entrée à court terme et un identificateur d’entrée à long terme et ces identificateurs peuvent ou ne peuvent pas identifier le même objet. Pour éviter de traitement redondant, appelez la méthode [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) pour comparer ces identificateurs d’entrée. Vous devez utiliser cette méthode pour la comparaison d’identificateur d’entrée, car les identificateurs d’entrée ne peut pas être comparées directement. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

