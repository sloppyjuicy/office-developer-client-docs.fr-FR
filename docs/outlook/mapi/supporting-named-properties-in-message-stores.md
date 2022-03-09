---
title: Prise en charge des propri�t�s nomm�es dans des magasins de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
ms.openlocfilehash: 9481769f72a3b5831e62d16f49788e530978996b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380136"
---
# <a name="supporting-named-properties-in-message-stores"></a>Prise en charge des propri�t�s nomm�es dans des magasins de Message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [D�finition des nouvelles propri�t�s MAPI](defining-new-mapi-properties.md) and [Prise en charge des propri�t�s nomm�es](supporting-named-properties.md).
  
Fournisseurs qui prennent en charge de nomm�e propri�t�s utiliser une signature de mappage unique pour tous les objets dans la banque d'informations de base de la plupart des messages. Cela a deux avantages. Tout d'abord, il est plus simple � impl�menter des signatures de mappage s'il en existe uniquement pour suivre. Deuxi�mement, si tous les objets dans la banque de messages utilisent la m�me signature de mappage, les applications clientes sont assur�es que tous les identificateurs de propri�t� sur les messages de la banque de messages font r�f�rent � la m�me propri�t� nomm�e. Cela permet aux applications de client afficher les colonnes de propri�t�s nomm�es dans son interface d'affichage de dossier.
  
## <a name="see-also"></a>Voir aussi



[Implémentation des messages dans les banques de messages](implementing-messages-in-message-stores.md)

