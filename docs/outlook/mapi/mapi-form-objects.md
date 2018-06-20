---
title: Objets de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784619"
---
# <a name="mapi-form-objects"></a>Objets de formulaire MAPI

  
  
**S’applique à**: Outlook 
  
Objets de formulaire sont créés dynamiquement par les serveurs de formulaire afin d’afficher des messages spécifiques et permettre aux utilisateurs d’interagir avec eux. Un objet form est, par conséquent, une instanciation de la classe dérivée [IMAPIForm](imapiformiunknown.md) qui est implémentée par le serveur de formulaire. Lorsqu’une application cliente ouvre un message, le serveur de formulaire pour cette classe de message crée un objet de formulaire pour gérer le message. L’objet form crée son interface et affiche les propriétés du message de celui-ci. L’objet de formulaire et son interface persiste jusqu'à ce que l’utilisateur le ferme. L’objet de formulaire gère toutes les modifications dans les valeurs des propriétés du message. 
  
En outre, les interfaces de formulaire MAPI définissent un mécanisme par lequel un objet form charger et afficher une série de messages. Il s’agit d’un mécanisme d’efficacité, car cela évite le destruction inutile et la création d’objets de message et leurs interfaces. Lorsque demandée par le client de messagerie pour charger un autre message, l’objet de formulaire doit enregistrer toutes les modifications aux propriétés du message en cours.
  
Pour plus d’informations sur le point de vue d’une application client des objets de formulaire, voir [MAPI aux objets formulaire personnalisé](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

