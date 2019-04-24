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
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327383"
---
# <a name="tnef-stream-structure"></a>Structure de flux TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un flux TNEF commence par une signature de 32 bits qui identifie le flux en tant que flux TNEF. Le suivi de la signature est un entier non signé 16 bits qui est utilisé comme clé pour effectuer une référence croisée des pièces jointes à leur emplacement dans le texte du message balisé. Le reste du flux est une séquence d'attributs TNEF. Les attributs de message apparaissent en premier dans le flux TNEF, et les attributs de pièces jointes suivent. Les attributs appartenant à une pièce jointe particulière sont regroupés ensemble, en commençant par l'attribut **attAttachRenddata** . 
  
La plupart des valeurs de constante utilisées dans les flux TNEF sont définies dans le format TNEF. Fichier d'en-tête H. En particulier, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**et tous les identificateurs d'attribut TNEF sont définis dans ce fichier. Les autres constantes ont les valeurs indiquées par leur interprétation d'un compilateur de langage C. En règle générale, ces constantes sont utilisées pour donner la taille de l'élément suivant. Par exemple, **sizeof (ULONG)** dans la définition d'un élément indique qu'un entier représentant la taille de l'entier long non signé suivant doit se produire à cet emplacement dans le flux TNEF. 
  
Tous les entiers d'un flux TNEF sont stockés au format binaire Little-endian, mais ils sont affichés au format hexadécimal dans cette section. Les valeurs de checksum sont simplement des entiers non signés 16 bits qui représentent la somme, Modulo 65536, des octets de données auxquels le checksum s'applique. Toutes les longueurs d'attribut sont des entiers longs non signés, y compris les caractères null de fin.
  
La clé est un entier non signé 16 bits différent de zéro qui indique la valeur initiale des clés de référence des pièces jointes. Les clés de référence des pièces jointes sont affectées de manière séquentielle à chaque pièce jointe en commençant par la valeur initiale qui est transmise à la fonction [OpenTnefStream](opentnefstream.md) par le fournisseur de services qui utilise le format TNEF. Le fournisseur de services doit générer une valeur initiale aléatoire pour la clé afin de réduire le risque que deux messages utilisent la même clé. 
  
L'implémentation TNEF utilise des identificateurs d'attribut pour mapper les attributs aux propriétés MAPI correspondantes. Un identificateur d'attribut est un entier non signé 32 bits composé de deux valeurs de Word. Le mot de poids fort indique le type de données, tel que String ou Binary, et le mot de poids faible identifie l'attribut particulier. Les types de données dans le mot de poids fort sont les suivants:
  
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
   
Les valeurs de mot de poids faible de chaque attribut sont définies dans le format TNEF. Fichier d'en-tête H.
  

