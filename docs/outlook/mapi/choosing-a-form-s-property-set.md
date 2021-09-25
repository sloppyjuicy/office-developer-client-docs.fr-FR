---
title: Sélection d’un ensemble de propriétés pour un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b18ac45fe04f1e299199e4a51bf952856d5bd85d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584723"
---
# <a name="choosing-a-forms-property-set"></a>Sélection d’un ensemble de propriétés pour un formulaire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous implémentez votre serveur de formulaires, vous devez avoir une propriété pour chaque information dont votre classe de message a besoin. Ces propriétés peuvent être des propriétés MAPI prédéfinie ou des propriétés personnalisées que vous définissez. Pour plus d’informations sur l’working with properties, voir [MAPI Property Overview](mapi-property-overview.md).
  
Votre fichier de configuration de formulaire contient une liste des propriétés que votre serveur de formulaires expose pour que les applications clientes l’utilisent, mais il ne doit pas s’agit de la liste complète des propriétés utilisées par votre serveur de formulaires. Les applications clientes utilisent généralement les propriétés exposées pour permettre aux utilisateurs de trier des messages dans un dossier ou de personnaliser leurs interfaces d’une manière ou d’une autre.
  
MAPI possède un grand ensemble de propriétés prédéfinie qui suffisent pour la plupart des applications. Toutefois, dans certains cas, une classe de message personnalisée a besoin d’une propriété que MAPI ne définit pas. Vous pouvez utiliser des propriétés personnalisées pour étendre l’ensemble prédéféré MAPI des informations spéciales que votre serveur de formulaires doit prendre en charge.
  
Vous pouvez utiliser l’une des méthodes suivantes pour définir des propriétés personnalisées :
  
- Choisissez un nom pour la propriété et utilisez la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir une balise de propriété pour elle. [L’interface IMAPIProp](imapipropiunknown.md) par le biais de laquelle vous appelez cette méthode provient du pointeur [IMessage](imessageimapiprop.md) qui est transmis au serveur de formulaire lors de la création du message. Notez que le nom de la propriété doit être une chaîne de caractères larges. 
    
- Définissez vous-même une balise de propriété personnalisée. Les balises de propriété personnalisée doivent se trouver dans la plage 0x6800 à 0x7BFF. Les propriétés de cette plage sont spécifiques aux classes de message.
    
Pour plus d’informations sur la définition de propriétés personnalisées, voir [Defining New MAPI Properties](defining-new-mapi-properties.md).
  
> [!NOTE]
> Les serveurs de formulaires qui ont un texte de message utilisent **souvent la propriété PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) pour le stocker. Si votre serveur de formulaires utilise **PR_RTF_COMPRESSED,** il doit également s’assurer que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contient une version texte uniquement du texte du message, au cas où le message résultant serait lu par un client qui ne prend pas en charge le texte rtf (Rich Text Format). 
  
## <a name="see-also"></a>Voir aussi

- [Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

