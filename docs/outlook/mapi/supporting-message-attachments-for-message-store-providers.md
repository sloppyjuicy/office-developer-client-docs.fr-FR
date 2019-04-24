---
title: Prise en charge des pièces jointes pour les fournisseurs de banques de messages
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350623"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Prise en charge des pièces jointes pour les fournisseurs de banques de messages

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre fournisseur de banque de messages n'a pas besoin de prendre en charge les pièces jointes des messages. Toutefois, de nombreuses applications clientes s'attendent à pouvoir ajouter des pièces jointes aux messages. Si votre magasin de messages doit être utilisé pour créer ou stocker IPM. Notez les messages, puis prenez en charge les pièces jointes des messages. Les fournisseurs de banques de messages par défaut doivent également prendre en charge les pièces jointes des messages. Pour plus d'informations, consultez la rubrique [classes de messages MAPI](mapi-message-classes.md)et [banques de messages par défaut](default-message-stores.md).
  
MAPI prend en charge cinq types de pièces jointes: les pièces jointes, les pièces jointes, les pièces jointes, les pièces jointes et les liens. Les conditions requises pour la prise en charge de chaque type sont différentes. Les clients différencient les deux types de pièces jointes par le biais de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) sur les objets Attachment.
  
La prise en charge des pièces jointes implique l'implémentation de l'interface [IAttach: IMAPIProp](iattachimapiprop.md) . L'interface **IAttach** ne possède pas de méthode propre; elle possède uniquement des méthodes qui sont héritées de l'interface [IMAPIProp](imapipropiunknown.md) . Étant donné que votre fournisseur de banque de messages doit déjà implémenter les propriétés pour les objets message, cela simplifie considérablement la tâche de prise en charge des pièces jointes. L'implémentation de **IAttach** signifie que les clients peuvent accéder à une table de propriétés pour des pièces jointes spécifiques sur les messages. 
  
Les pièces jointes de données sont simplement des pièces jointes pour lesquelles le contenu de la pièce jointe est stocké directement dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d'une pièce jointe. Les pièces jointes de données existent principalement pour permettre aux clients de joindre des fichiers à un message lorsque l'expéditeur et le destinataire du message n'ont pas accès à un serveur de fichiers commun. Pour plus d'informations, reportez-vous à la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Les pièces jointes des messages sont des pièces jointes pour lesquelles le sous-objet de pièce jointe est un autre objet [IMessage: MAPIProp](imessageimapiprop.md) . Comme les fournisseurs de banque de messages prennent déjà en charge l'interface **IMessage** , la prise en charge des pièces jointes des messages n'est pas difficile. 
  
La prise en charge des pièces jointes des objets OLE implique l'implémentation des interfaces OLE **IStorage**, **IStream**et **IStreamDocfile** . Votre fournisseur de banque de messages doit pouvoir convertir les données d'objets OLE stockées dans le message en un objet OLE actif lorsqu'un client ouvre l'objet. 
  
Il existe deux types de liens: des liens vers des fichiers et des liens vers d'autres messages. Liens vers des fichiers utilisez la valeur ATTACH_BY_REF_ONLY pour la propriété **PR_ATTACH_METHOD** avec **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) pour spécifier emplacement d'un fichier.
  
Le mode d'implémentation des liens vers les messages peut dépendre des aspects du système de messagerie local et, en tant que tel, ne peut pas être entièrement documenté ici. Par exemple, l'envoi d'un lien vers un message qui est stocké dans une banque de messages basée sur le serveur est généralement une question d'envoi de l'identificateur d'entrée du message lié, à condition que l'expéditeur et le destinataire aient accès à ce serveur. Les autres configurations de système de messagerie présentent d'autres exigences et défis en matière d'implémentation de liens vers des messages.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

