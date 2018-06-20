---
title: Structure de flux TNEF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0fcd1c79d1c0debfb18d270dc0e40de42842c6d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787369"
---
# <a name="tnef-stream-structure"></a>Structure de flux TNEF

  
  
**S’applique à**: Outlook 
  
Un flux TNEF commence avec une signature 32 bits qui identifie le flux sous forme de flux TNEF. La signature est un entier non signé de 16 bits qui est utilisé comme une clé pour le renvoi des pièces jointes à leur emplacement dans le texte du message avec balise. Le reste du flux est une séquence d’attributs TNEF. Attributs de message apparaissent en premier dans le flux TNEF et suivent les attributs de pièce jointe. Attributs appartenant à une pièce jointe particulier sont regroupées, à partir de l’attribut **attAttachRenddata** . 
  
La plupart des valeurs de constante utilisées dans des flux TNEF est définie dans le format TNEF. Fichier d’en-tête H. En particulier, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**et tous les identificateurs d’attribut TNEF sont définies dans ce fichier. Autres constantes possèdent les valeurs indiquées par leur interprétation à un compilateur de langage C. En règle générale, ces constantes sont utilisées pour donner à la taille de l’élément suivant. Par exemple, **sizeof** dans la définition d’un élément indique qu’un entier représentant la taille de l’entier long non signé suivant doit se produire à cet endroit dans le flux TNEF. 
  
Tous les entiers dans un flux TNEF sont stockés sous forme binaire primauté, mais sont affichées au format hexadécimal dans cette section. Les valeurs de somme de contrôle sont des entiers simplement 16 bits sont les fonctions sum, modulo 65536, d’octets de données correspondant à la somme de contrôle. Toutes les longueurs d’attribut sont des entiers longs, y compris tout caractère null de fin.
  
La clé est un entier non signé différente de zéro, 16 bits qui indique la valeur initiale de clés de référence de pièce jointe. Clés de référence des pièces jointes sont affectées à chaque pièce jointe en séquence commençant par la valeur initiale est transmise à la fonction [OpenTnefStream](opentnefstream.md) par le fournisseur de services qui est à l’aide de TNEF. Le fournisseur de services doit générer une valeur initiale aléatoire pour la clé réduire le risque que deux messages utilisent la même clé. 
  
L’implémentation de TNEF utilise les identificateurs des attributs pour mapper les attributs sur des propriétés MAPI correspondantes. Un identificateur d’attribut est un entier non signé 32 bits composé de deux valeurs de word. Le mot d’ordre haut indique le type de données, telles que la chaîne ou binaire, et le mot de poids faible identifie l’attribut particulier. Les types de données dans le mot de poids fort sont les suivants :
  
|**Type**|**Valeur**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0 x 0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0 x 0009  <br/> |
   
Les valeurs de mot de poids faible de chaque attribut sont définies dans le format TNEF. Fichier d’en-tête H.
  

