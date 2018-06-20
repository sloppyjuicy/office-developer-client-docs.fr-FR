---
title: Texte du Message TNEF balisés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787362"
---
# <a name="tnef-tagged-message-text"></a>Texte du Message TNEF balisés

  
  
**S’applique à**: Outlook 
  
Texte du message avec balise est utilisé par TNEF pour résoudre les positions des pièces jointes dans le message parent. Cette opération est effectuée en ajoutant un espace réservé dans le texte du message à la position de la pièce jointe. Cet espace réservé ou balise de pièce jointe, décrit la pièce jointe de telle sorte que TNEF sait comment résoudre la pièce jointe et sa position. Les balises sont mis en forme comme suit :
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 ** \<Objet titre\> ** et ** \<nom de fichier\> ** sont des variables qui contiennent des valeurs qui proviennent de la pièce jointe elle-même. Dans les cas où ces valeurs ne sont pas disponibles, le titre par défaut est celle par TNEF en fonction du type de pièce jointe. 
  
Le ** \<KeyNum\> ** variable contient la représentation textuelle de la clé de pièce jointe associée à la pièce jointe par le format TNEF. La valeur de la clé de base est transmise à l’appel de [OpenTnefStreamEx](opentnefstreamex.md) . La valeur de base ne doit pas être zéro et ne doit pas être la même pour chaque appel à **OpenTnefStreamEx**. Elle devrait suffire pour utiliser des nombres aléatoires pseudo en fonction de l’heure système dans le Générateur de nombres aléatoires votre bibliothèque d’exécution fournit, dans la mesure où vous assurer qu’ils ne sont jamais zéro.
  
Le ** \<nom Transport\> ** variable contient le nom de flux de données passé dans l’appel [OpenTnefStreamEx](opentnefstreamex.md) ou la valeur de la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> La propriété **PR_ATTACH_TRANSPORT_NAME** et ** \<nom Transport\> ** variable dans une balise de texte de message n’a rien à voir avec le nom du fournisseur de transport que vous implémentez. Ces éléments représentent le nom d’une pièce jointe pour le fournisseur de transport et le système de messagerie. 
  
Le texte du message est marqué à la demande à un fournisseur de transport pour le texte du message avec balise en appelant la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . Lors de la lecture à partir du flux de texte référencé, TNEF remplace le caractère unique dans le texte du message à l’index fourni dans la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) avec la balise appropriée. Lors de l’écriture dans le flux de texte référencé, TNEF vérifie les données entrantes pour les balises, trouve la pièce jointe associée et remplace la balise par un seul espace.
  
Notez que, en utilisant le texte du message avec balise, un fournisseur de transport permettre conserver le positionnement des pièces jointes quelle que soit la plupart des modifications apportées au texte du message par les systèmes de messagerie.
  

