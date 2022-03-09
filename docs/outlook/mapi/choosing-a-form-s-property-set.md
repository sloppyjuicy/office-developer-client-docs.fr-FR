---
title: Sélection d’un ensemble de propriétés pour un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
ms.openlocfilehash: 361fab1d6342bcc46d914513b07e48a6d100f18c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370469"
---
# <a name="choosing-a-forms-property-set"></a>Sélection d’un ensemble de propriétés pour un formulaire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous implémentez votre serveur de formulaires, vous devez avoir une propriété pour chaque information dont votre classe de message a besoin. Ces propriétés peuvent être des propriétés MAPI prédéfinie ou des propriétés personnalisées que vous définissez. Pour plus d’informations sur l’working with properties, voir [MAPI Property Overview](mapi-property-overview.md).
  
Votre fichier de configuration de formulaire contient une liste des propriétés que votre serveur de formulaires expose pour que les applications clientes l’utilisent, mais il ne doit pas s’agit de la liste complète des propriétés utilisées par votre serveur de formulaires. Les applications clientes utilisent généralement les propriétés exposées pour permettre aux utilisateurs de trier des messages dans un dossier ou de personnaliser leurs interfaces d’une manière ou d’une autre.
  
MAPI possède un grand ensemble de propriétés prédéfinie qui suffisent pour la plupart des applications. Toutefois, il peut se passer qu’une classe de message personnalisée nécessite une propriété que MAPI ne définit pas. Vous pouvez utiliser des propriétés personnalisées pour étendre l’ensemble de propriétés mapi prédéfinis pour toutes les informations spéciales que votre serveur de formulaires doit prendre en charge.
  
Vous pouvez utiliser l’une des méthodes suivantes pour définir des propriétés personnalisées :
  
- Choisissez un nom pour la propriété et utilisez la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir une balise de propriété pour cette propriété. [L’interface IMAPIProp](imapipropiunknown.md) par le biais de laquelle vous appelez cette méthode provient du pointeur [IMessage](imessageimapiprop.md) qui est transmis au serveur de formulaire lors de la création du message. Notez que le nom de la propriété doit être une chaîne de caractères larges. 
    
- Définissez vous-même une balise de propriété personnalisée. Les balises de propriété personnalisée doivent se trouver dans la plage 0x6800 à 0x7BFF. Les propriétés de cette plage sont spécifiques aux classes de message.
    
Pour plus d’informations sur la définition de propriétés personnalisées, voir [Defining New MAPI Properties](defining-new-mapi-properties.md).
  
> [!NOTE]
> Les serveurs de formulaires qui ont un texte de message utilisent **PR_RTF_COMPRESSED** propriété ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) pour le stocker. Si votre serveur de formulaires utilise **PR_RTF_COMPRESSED**, il doit également s’assurer que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contient une version texte uniquement du texte du message, au cas où le message résultant serait lu par un client qui ne prend pas en charge le texte rtf (Rich Text Format). 
  
## <a name="see-also"></a>Voir aussi

- [Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

