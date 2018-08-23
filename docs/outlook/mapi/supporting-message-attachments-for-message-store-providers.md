---
title: Prise en charge des pièces jointes de message pour les fournisseurs de banques de messages
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: a94d1230f4f26d080976fd15768bdfeb6ea04748
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576098"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Prise en charge des pièces jointes de message pour les fournisseurs de banques de messages

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Votre fournisseur de magasin de message n’a pas besoin prendre en charge les pièces jointes des messages. Toutefois, de nombreuses applications clientes prévoient être en mesure d’ajouter des pièces jointes aux messages. Si votre banque de messages doit être utilisée pour créer ou stocker IPM. Remarque Les messages, puis vous devez prendre en charge des pièces jointes des messages. Fournisseurs de banque de message par défaut doivent prennent également en charge les pièces jointes des messages. Pour plus d’informations, consultez [Classes de Message MAPI](mapi-message-classes.md)et [Banques de Message par défaut](default-message-stores.md).
  
Il existe cinq types de pièces jointes qui prend en charge de MAPI : fichiers de pièces jointes, les pièces jointes de données, pièces jointes des messages, les pièces jointes objet OLE et des liens. La configuration requise pour chaque type de prise en charge est différente. Clients fait aucune différence entre les deux types de pièces jointes au moyen de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) sur les objets de la pièce jointe.
  
Prise en charge des pièces jointes signifie mettre en œuvre la [IAttach : IMAPIProp](iattachimapiprop.md) interface. L’interface **IAttach** possède pas de méthodes qui lui est propre ; il dispose uniquement de méthodes héritées de l’interface [IMAPIProp](imapipropiunknown.md) . Parce que votre fournisseur de magasin de message doit implémenter déjà les propriétés d’objets de message, cela simplifie grandement la tâche de prise en charge des pièces jointes. Implémentation **IAttach** fondamentalement revient à fournir un moyen pour les clients pour accéder à une table de propriétés pour les pièces jointes des messages. 
  
Pièces jointes sont simplement les pièces jointes dont le contenu de la pièce jointe est stocké directement dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de la pièce jointe. Pièces jointes de données existent principalement pour permettre aux clients de joindre des fichiers à un message lors de l’expéditeur et le destinataire du message n’ont pas accès à un serveur de fichiers communs. Pour plus d’informations, voir la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Pièces jointes des messages sont des pièces jointes pour laquelle le sous-objet de pièce jointe est un autre [IMessage : MAPIProp](imessageimapiprop.md) objet. Étant donné que les fournisseurs de banque de messages prennent déjà en charge l’interface **IMessage** , la prise en charge des pièces jointes des messages n’est pas difficile. 
  
Prise en charge les pièces jointes OLE object signifie implémenter les interfaces OLE **IStorage** **IStream**et **IStreamDocfile** . Votre fournisseur de magasin de message doit être en mesure de convertir les données stockées dans le message dans un objet OLE actif lorsqu’un client ouvre l’objet de l’objet OLE. 
  
Liens sont de deux types : liens vers des fichiers et des liens vers d’autres messages. Liens vers des fichiers utilisent la valeur ATTACH_BY_REF_ONLY pour la propriété **PR_ATTACH_METHOD** ainsi que **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) pour spécifier l’emplacement d’un fichier.
  
Comment un implémente des liens vers les messages peut-être dépendre des aspects du système de messagerie local et, par conséquent, ne peut pas être entièrement documenté ici. Par exemple, l’envoi d’un lien à un message qui est stocké dans une banque de messages sur le serveur est généralement qu’une question de l’envoi de l’identificateur d’entrée du message lié, fournissant que l’expéditeur et le destinataire ont accès à ce serveur. Autres configurations de système de messagerie présentent les autres exigences et les défis pour l’implémentation des liens vers des messages.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

