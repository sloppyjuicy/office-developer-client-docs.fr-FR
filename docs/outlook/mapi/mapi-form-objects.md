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
  
Les objets de formulaire sont créés dynamiquement par les serveurs de formulaires afin d’afficher des messages spécifiques et permettre aux utilisateurs d’interagir avec eux. Un objet de formulaire est, par conséquent, une ins instantiation de la classe dérivée [d’IMAPIForm](imapiformiunknown.md) qui est implémentée par le serveur de formulaires. Lorsqu’une application cliente ouvre un message, le serveur de formulaires de cette classe de message crée un objet de formulaire pour gérer le message. L’objet formulaire crée ensuite son interface et y affiche les propriétés du message. L’objet de formulaire et son interface persistent jusqu’à ce que l’utilisateur le ferme. L’objet de formulaire gère les modifications apportées aux valeurs des propriétés du message. 
  
En outre, les interfaces de formulaire MAPI définissent un mécanisme par lequel un objet de formulaire peut charger et afficher une série de messages. Il s’agit d’un mécanisme d’efficacité, car il évite la destruction inutile et la création d’objets de message et de leurs interfaces. Lorsque le client de messagerie demande le chargement d’un autre message, l’objet formulaire doit enregistrer les modifications apportées aux propriétés du message actuel.
  
Pour plus d’informations sur la perspective des objets de formulaire d’une application cliente, voir [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

