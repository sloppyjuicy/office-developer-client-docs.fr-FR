---
title: Sélection d’un ensemble de propriétés pour un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332059"
---
# <a name="choosing-a-forms-property-set"></a>Sélection d’un ensemble de propriétés pour un formulaire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous implémentez votre serveur de formulaire, vous devez disposer d'une propriété pour chaque information dont votre classe de message a besoin. Ces propriétés peuvent être des propriétés MAPI prédéfinies ou des propriétés personnalisées que vous définissez. Pour plus d'informations sur l'utilisation des propriétés, voir [MAPI Property Overview](mapi-property-overview.md).
  
Votre fichier de configuration de formulaire contiendra une liste de propriétés que votre serveur de formulaire expose pour les applications clientes à utiliser, mais cela ne doit pas nécessairement être la liste complète des propriétés utilisées par votre serveur de formulaires. Les applications clientes utilisent généralement les propriétés exposées pour permettre aux utilisateurs de trier les messages d'un dossier ou de personnaliser leurs interfaces d'une certaine façon.
  
MAPI dispose d'un grand ensemble de propriétés prédéfinies qui suffisent à la plupart des applications. Toutefois, il arrivera qu'une classe de message personnalisée ait besoin d'une propriété non définie par MAPI. Vous pouvez utiliser des propriétés personnalisées pour étendre l'ensemble prédéfini MAPI de propriétés pour les informations spéciales que votre serveur de formulaire doit prendre en charge.
  
Vous pouvez utiliser l'une des méthodes suivantes pour définir des propriétés personnalisées:
  
- Choisissez un nom pour la propriété et utilisez la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir une balise de propriété. L'interface [IMAPIProp](imapipropiunknown.md) par le biais de laquelle vous appelez cette méthode provient du pointeur [IMessage](imessageimapiprop.md) transmis au serveur de formulaire lors de la création du message. Notez que le nom de la propriété doit être une chaîne à caractères larges. 
    
- Définissez une balise de propriété personnalisée vous-même. Les balises de propriété personnalisée doivent être comprises dans la plage 0x6800 à 0x7BFF. Les propriétés de cette plage sont spécifiques à la classe de messages.
    
Pour plus d'informations sur la définition des propriétés personnalisées, consultez la rubrique [Defining New MAPI Properties](defining-new-mapi-properties.md).
  
> [!NOTE]
> Les serveurs de formulaire qui ont un texte de message utilisent souvent la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) pour le stocker. Si votre serveur de formulaire utilise **PR_RTF_COMPRESSED**, il doit également s'assurer que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contient une version de texte uniquement du texte du message, dans le cas où le message résultant est lu par un client qui ne prend pas en charge le texte enrichi. Texte du message au format (RTF). 
  
## <a name="see-also"></a>Voir aussi

- [Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

