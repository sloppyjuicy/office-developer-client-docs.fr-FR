---
title: TNEF-Tagged texte du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419918"
---
# <a name="tnef-tagged-message-text"></a>TNEF-Tagged texte du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le texte du message marqué est utilisé par le TNEF pour résoudre les positions des pièces jointes dans le message parent. Pour ce faire, ajoutez un titulaire de position dans le texte du message à la position de la pièce jointe. Ce support d’endroit, ou balise de pièce jointe, décrit la pièce jointe de telle sorte que le TNEF sache comment résoudre la pièce jointe et sa position. Les balises sont formatées comme suit :
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\< Le \> titre de l’objet** et **\< le nom de \>** fichier sont des variables contenant des valeurs qui sont tirées de la pièce jointe elle-même. Dans les cas où ces valeurs ne sont pas disponibles, le titre est par défaut au TNEF en fonction du type de pièce jointe. 
  
La variable **\< KeyNum \>** contient la représentation textuelle de la clé de pièce jointe affectée à la pièce jointe par le TNEF. La valeur de base de la clé est transmise à [l’appel OpenTnefStreamEx.](opentnefstreamex.md) La valeur de base ne doit pas être zéro et ne doit pas être identique pour chaque appel à **OpenTnefStreamEx**. Il suffit d’utiliser des nombres pseudo-aléatoires en fonction de l’heure système à partir du générateur de nombres aléatoires que votre bibliothèque d’utilisation fournit, à condition que vous garantissez qu’ils ne sont jamais nuls.
  
La variable **\< Nom \>** de transport contient le nom du flux transmis à l’appel [OpenTnefStreamEx](opentnefstreamex.md) ou la valeur de la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> La **PR_ATTACH_TRANSPORT_NAME** de transport et la variable **\< de \>** nom de transport dans une balise de texte de message n’ont rien à voir avec le nom du fournisseur de transport que vous implémentez. Ces éléments représentent le nom d’une pièce jointe pour le fournisseur de transport et le système de messagerie. 
  
Le texte du message est balisé lorsqu’un fournisseur de transport demande un texte de message marqué en appelant la méthode [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md) Lors de la lecture à partir du flux de texte balisé, TNEF remplace le caractère unique qui se trouvait dans le texte du message à l’index fourni dans la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) par la balise appropriée. Lors de l’écriture dans le flux de texte balisé, le TNEF recherche les balises dans les données entrantes, recherche la pièce jointe associée et remplace la balise par un espace unique.
  
Notez qu’à l’aide de texte de message balisé, un fournisseur de transport peut conserver le positionnement des pièces jointes indépendamment de la plupart des modifications apportées au texte du message par les systèmes de messagerie.
  

