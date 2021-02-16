---
title: Prise en charge des pièces jointes de messages pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412134"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Prise en charge des pièces jointes de messages pour les fournisseurs de magasins de messages

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre fournisseur de magasins de messages n’a pas besoin de prendre en charge les pièces jointes des messages. Toutefois, de nombreuses applications clientes s’attendent à pouvoir ajouter des pièces jointes à des messages. Si votre magasin de messages est utilisé pour créer ou stocker un IPM. Notez les messages, puis vous devez prendre en charge les pièces jointes des messages. Les fournisseurs de magasins de messages par défaut doivent également prendre en charge les pièces jointes des messages. Pour plus d’informations, voir Classes de [messages MAPI](mapi-message-classes.md)et [Magasins de messages par défaut.](default-message-stores.md)
  
MAPI prend en charge cinq types de pièces jointes : pièces jointes, pièces jointes de données, pièces jointes de message, pièces jointes d’objets OLE et liens. Les conditions requises pour la prise en charge de chaque type sont différentes. Les clients différencient les deux types de pièces jointes au moyen de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) sur les objets de pièce jointe.
  
La prise en charge des pièces jointes implique l’implémentation de l’interface [IAttach : IMAPIProp.](iattachimapiprop.md) **L’interface IAttach** n’a aucune méthode propre ; Il possède uniquement des méthodes qui sont héritées de l’interface [IMAPIProp.](imapipropiunknown.md) Étant donné que votre fournisseur de magasin de messages doit déjà implémenter des propriétés pour les objets de message, cela simplifie considérablement la tâche de prise en charge des pièces jointes. **L’implémentation d’IAttach** signifie essentiellement fournir aux clients un moyen d’accéder à une table de propriétés pour des pièces jointes particulières sur des messages. 
  
Les pièces jointes de données sont simplement des pièces jointes pour lesquelles le contenu de la pièce jointe est stocké directement dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d’une pièce jointe. Les pièces jointes de données existent principalement pour permettre aux clients d’attacher des fichiers à un message lorsque l’expéditeur et le destinataire du message n’ont pas accès à un serveur de fichiers commun. Pour plus d’informations, **voir la PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Les pièces jointes de message sont des pièces jointes dont le sous-objet de pièce jointe est un autre [objet IMessage : MAPIProp.](imessageimapiprop.md) Étant donné que les fournisseurs de magasins de messages supportent déjà l’interface **IMessage,** la prise en charge des pièces jointes de message n’est pas difficile. 
  
La prise en charge des pièces jointes d’objet OLE implique l’implémentation des interfaces OLE **IStorage,** **IStream** et **IStreamDocfile.** Votre fournisseur de magasins de messages doit être en mesure de convertir les données d’objet OLE stockées dans le message en objet OLE actif lorsqu’un client ouvre l’objet. 
  
Les liens sont de deux types : liens vers des fichiers et liens vers d’autres messages. Les liens vers des fichiers utilisent la valeur ATTACH_BY_REF_ONLY pour la propriété **PR_ATTACH_METHOD** avec **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) pour spécifier l’emplacement d’un fichier.
  
La façon dont une personne implémente des liens vers des messages peut dépendre d’aspects du système de messagerie local et, en tant que telle, ne peut pas être entièrement documentée ici. Par exemple, l’envoi d’un lien vers un message stocké sur un magasin de messages basé sur un serveur n’est généralement qu’une question d’envoi de l’identificateur d’entrée du message lié, à condition que l’expéditeur et le destinataire ont accès à ce serveur. D’autres configurations de système de messagerie présentent d’autres exigences et défis pour l’implémentation de liens vers des messages.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

