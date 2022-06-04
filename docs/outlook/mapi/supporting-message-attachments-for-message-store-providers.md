---
title: Prise en charge des pièces jointes de message pour les fournisseurs de magasin de messages
description: Décrit cinq types de pièces jointes prises en charge par MAPI, notamment les pièces jointes de fichier, les pièces jointes de données, les pièces jointes de message, les pièces jointes d’objet OLE et les liens.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
ms.openlocfilehash: 89eec531c33283039a38214b09bfcdc49e0af8eb
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893640"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Prise en charge des pièces jointes de message pour les fournisseurs de magasin de messages

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre fournisseur de magasin de messages n’a pas besoin de prendre en charge les pièces jointes de message. Toutefois, de nombreuses applications clientes s’attendent à pouvoir ajouter des pièces jointes aux messages. Si votre magasin de messages sera utilisé pour créer ou stocker des IPM. Notez les messages, puis vous devez prendre en charge les pièces jointes de message. Les fournisseurs de magasins de messages par défaut doivent également prendre en charge les pièces jointes de message. Pour plus d’informations, consultez [classes de message MAPI et Magasins](mapi-message-classes.md) de [messages par défaut](default-message-stores.md).
  
MapI prend en charge cinq types de pièces jointes : les pièces jointes de fichier, les pièces jointes de données, les pièces jointes de message, les pièces jointes d’objet OLE et les liens. Les conditions requises pour la prise en charge de chaque type sont différentes. Les clients différencient les deux types de pièces jointes par le biais de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) sur les objets de pièce jointe.
  
La prise en charge des pièces jointes implique l’implémentation de l’interface [IAttach : IMAPIProp](iattachimapiprop.md) . **L’interface IAttach** n’a pas de méthode propre ; il n’a que des méthodes héritées de l’interface [IMAPIProp](imapipropiunknown.md). Étant donné que votre fournisseur de magasin de messages doit déjà implémenter des propriétés pour les objets de message, cela simplifie considérablement la tâche de prise en charge des pièces jointes. L’implémentation **d’IAttach** consiste essentiellement à fournir un moyen aux clients d’accéder à une table de propriétés pour des pièces jointes particulières sur les messages. 
  
Les pièces jointes de données sont simplement des pièces jointes pour lesquelles le contenu de la pièce jointe est stocké directement dans la propriété **PR_ATTACH_DATA_BIN** d’une pièce jointe ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Les pièces jointes de données existent principalement pour permettre aux clients d’attacher des fichiers à un message lorsque l’expéditeur et le destinataire du message n’ont pas accès à un serveur de fichiers commun. Pour plus d’informations, consultez la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Les pièces jointes de message sont des pièces jointes pour lesquelles le sous-objet de pièce jointe est un autre objet [IMessage : MAPIProp](imessageimapiprop.md) . Étant donné que les fournisseurs de magasins de messages prennent déjà en charge l’interface **IMessage** , la prise en charge des pièces jointes de message n’est pas difficile. 
  
La prise en charge des pièces jointes d’objet OLE implique l’implémentation des interfaces OLE **IStorage**, **IStream** et **IStreamDocfile** . Votre fournisseur de magasin de messages doit être en mesure de convertir les données d’objet OLE stockées dans le message en objet OLE actif lorsqu’un client ouvre l’objet. 
  
Les liens sont de deux types : les liens vers les fichiers et les liens vers d’autres messages. Les liens vers des fichiers utilisent la valeur ATTACH_BY_REF_ONLY de la propriété **PR_ATTACH_METHOD** , ainsi que **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) pour spécifier l’emplacement d’un fichier.
  
La façon dont on implémente des liens vers des messages peut dépendre des aspects du système de messagerie local et, par conséquent, ne peut pas être entièrement documentée ici. Par exemple, l’envoi d’un lien vers un message stocké sur un magasin de messages serveur consiste généralement simplement à envoyer l’identificateur d’entrée du message lié, à condition que l’expéditeur et le destinataire aient accès à ce serveur. D’autres configurations du système de messagerie présentent d’autres exigences et défis pour l’implémentation de liens vers des messages.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

