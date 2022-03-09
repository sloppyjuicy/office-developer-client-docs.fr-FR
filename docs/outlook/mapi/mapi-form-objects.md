---
title: Objets de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
ms.openlocfilehash: 8119e85f0f187c863b0b4284b19bad8b886c4f0e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369104"
---
# <a name="mapi-form-objects"></a>Objets de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets de formulaire sont créés dynamiquement par les serveurs de formulaires afin d’afficher des messages spécifiques et permettre aux utilisateurs d’interagir avec eux. Un objet de formulaire est donc une ins instantiation de la classe dérivée [d’IMAPIForm](imapiformiunknown.md) qui est implémentée par le serveur de formulaires. Lorsqu’une application cliente ouvre un message, le serveur de formulaires de cette classe de message crée un objet de formulaire pour gérer le message. L’objet formulaire crée ensuite son interface et y affiche les propriétés du message. L’objet formulaire et son interface persistent jusqu’à ce que l’utilisateur le ferme. L’objet de formulaire gère les modifications apportées aux valeurs des propriétés du message. 
  
En outre, les interfaces de formulaire MAPI définissent un mécanisme par lequel un objet de formulaire peut charger et afficher une série de messages. Il s’agit d’un mécanisme d’efficacité, car il évite la destruction inutile et la création d’objets de message et de leurs interfaces. Lorsque le client de messagerie demande le chargement d’un autre message, l’objet formulaire doit enregistrer les modifications apportées aux propriétés du message actuel.
  
Pour plus d’informations sur la perspective des objets de formulaire d’une application cliente, voir [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

