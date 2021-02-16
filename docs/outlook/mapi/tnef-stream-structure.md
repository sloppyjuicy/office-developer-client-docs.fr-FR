---
title: Structure de flux TNEF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430202"
---
# <a name="tnef-stream-structure"></a>Structure de flux TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un flux TNEF commence par une signature 32 bits qui identifie le flux en tant que flux TNEF. À la suite de la signature se trouve un nombre d’éléments non signés 16 bits utilisé comme clé pour faire référence à des pièces jointes à leur emplacement dans le texte du message marqué. Le reste du flux est une séquence d’attributs TNEF. Les attributs de message apparaissent en premier dans le flux TNEF et les attributs de pièce jointe suivent. Les attributs qui appartiennent à une pièce jointe particulière sont regroupés, en commençant par l’attribut **attAttachRenddata.** 
  
La plupart des valeurs constantes utilisées dans les flux TNEF sont définies dans le TNEF. Fichier d’en-tête H. Notamment, **TNEF_SIGNATURE**, **LVL_MESSAGE,** **LVL_ATTACHMENT** et tous les identificateurs d’attribut TNEF sont définis dans ce fichier. Les autres constantes ont les valeurs indiquées par leur interprétation d’un compilateur de langage C. En règle générale, ces constantes sont utilisées pour donner la taille de l’élément suivant. Par exemple, **sizeof(ULONG)** dans la définition d’un élément indique qu’un nombre integer représentant la taille de l’objet long non signé suivant doit se produire à cet endroit dans le flux TNEF. 
  
Tous les nombres integers d’un flux TNEF sont stockés dans une forme binaire peu endian, mais sont affichés en hexadécimal tout au long de cette section. Les valeurs checksum sont simplement des nombres d’octets non signés de 16 bits qui sont la somme, modquet 65536, des octets de données à qui s’applique la somme de contrôle. Toutes les longueurs d’attribut sont des caractères longs non signés, y compris les caractères null qui se terminent.
  
La clé est un nombre non zéro, 16 bits non signé qui signifie la valeur initiale des clés de référence de pièce jointe. Les clés de référence de pièce jointe sont affectées à chaque pièce jointe de manière séquentielle en commençant par la valeur initiale qui est passée à la fonction [OpenTnefStream](opentnefstream.md) par le fournisseur de services qui utilise le TNEF. Le fournisseur de services doit générer une valeur initiale aléatoire pour la clé afin de réduire le risque que deux messages utilisent la même clé. 
  
L’implémentation TNEF utilise des identificateurs d’attributs pour ma cartographier les attributs à leurs propriétés MAPI correspondantes. Un identificateur d’attribut est un nombre non signé 32 bits composé de deux valeurs de mots. Le mot de haut niveau indique le type de données, tel que chaîne ou binaire, et le mot de bas ordre identifie l’attribut particulier. Les types de données dans le mot d’ordre élevé sont :
  
|**Type**|**Valeur**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0x0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0x0009  <br/> |
   
Les valeurs de mots de bas ordre pour chaque attribut sont définies dans le TNEF. Fichier d’en-tête H.
  

