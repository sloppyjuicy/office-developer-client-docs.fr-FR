---
title: Choix du jeu de propriétés d’un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 456ef036b26fd8b9840d33f0f699474c3a6ce127
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783042"
---
# <a name="choosing-a-forms-property-set"></a>Choix du jeu de propriétés d’un formulaire

**S’applique à**: Outlook 
  
Lorsque vous implémentez votre serveur de formulaire, vous devez avoir une propriété pour chaque élément d’information qui a besoin de votre classe de message. Ces propriétés peuvent être des propriétés MAPI prédéfinies, ou ils peuvent être des propriétés personnalisées que vous définissez. Pour plus d’informations sur l’utilisation des propriétés, voir [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md).
  
Votre fichier de configuration de formulaire contient une liste des propriétés qui expose de votre serveur de formulaire pour les applications clientes à utiliser, mais il ne doit pas être la liste complète des propriétés utilisées par le serveur de votre formulaire. Applications clientes utilisent généralement les propriétés exposées pour permettre aux utilisateurs de classer les messages dans un dossier ou personnaliser leurs interfaces d’une manière.
  
MAPI a un grand ensemble de propriétés prédéfinies qui suffit pour la plupart des applications. Toutefois, il peut arriver lorsqu’une classe de message personnalisée doit être une propriété qui ne définit pas de MAPI. Vous pouvez utiliser les propriétés personnalisées pour étendre l’ensemble MAPI prédéfinie des propriétés pour les informations spéciales que votre serveur de formulaire doit prendre en charge.
  
Vous pouvez utiliser une des méthodes suivantes pour définir des propriétés personnalisées :
  
- Choisissez un nom pour la propriété et la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) permet d’obtenir une balise de propriété pour celui-ci. L’interface [IMAPIProp](imapipropiunknown.md) par le biais de laquelle vous appelez cette méthode provient le pointeur [IMessage](imessageimapiprop.md) qui est transmis au serveur de formulaire lorsque le message est créé. Notez que le nom de la propriété doit être une chaîne de caractères étendus. 
    
- Définir une balise de propriété personnalisée vous-même. Balises de propriété personnalisée doivent être dans la plage 0x6800 via 0x7BFF. Les propriétés de cette plage sont classe de message spécifique.
    
Pour plus d’informations sur la définition des propriétés personnalisées, voir [Définition des nouvelles propriétés MAPI](defining-new-mapi-properties.md).
  
> [!NOTE]
> Serveurs de formulaire qui ont un texte de message souvent permet de stocker la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Si votre serveur formulaire utilise **PR_RTF_COMPRESSED**, il doit également vous assurer que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contient une version texte seul du texte du message, au cas où le message qui en résulte est lu par un client qui ne prend pas en charge le texte riche Texte du message au format RTF. 
  
## <a name="see-also"></a>Voir aussi

- [Développez serveurs de formulaire MAPI](developing-mapi-form-servers.md)

