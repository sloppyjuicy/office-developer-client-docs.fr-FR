---
title: Objets de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404784"
---
# <a name="mapi-form-objects"></a>Objets de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets de formulaire sont créés dynamiquement par les serveurs de formulaires afin d'afficher des messages spécifiques et d'autoriser les utilisateurs à interagir avec eux. Un objet Form est, par conséquent, une instanciation de la classe dérivée de [IMAPIForm](imapiformiunknown.md) qui est implémentée par le serveur de formulaire. Lorsqu'une application cliente ouvre un message, le serveur de formulaire pour cette classe de message crée un objet Form pour gérer le message. L'objet Form crée ensuite son interface et affiche les propriétés du message qu'elle contient. L'objet Form et son interface persistent jusqu'à ce que l'utilisateur le ferme. L'objet Form gère toutes les modifications apportées aux valeurs des propriétés du message. 
  
En outre, les interfaces de formulaire MAPI définissent un mécanisme par lequel un objet Form peut charger et afficher une série de messages. Il s'agit d'un mécanisme efficace, car il évite la destruction et la création d'objets message et de leurs interfaces inutiles. Lorsque le client de messagerie le demande de charger un autre message, l'objet Form doit enregistrer les modifications apportées aux propriétés du message actif.
  
Pour plus d'informations sur la perspective d'un objet de formulaire dans une application cliente, consultez la rubrique [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

