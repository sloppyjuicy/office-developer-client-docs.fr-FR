---
title: Structure de flux TNEF
description: Décrit la structure de flux TNEF. Cet article s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
ms.openlocfilehash: f86d00f0d3fd1446551fe208dfd7fb3da862ed3b
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894214"
---
# <a name="tnef-stream-structure"></a>Structure de flux TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un flux TNEF commence par une signature 32 bits qui identifie le flux en tant que flux TNEF. Après la signature se trouve un entier non signé 16 bits qui est utilisé comme clé pour référencer des pièces jointes croisées à leur emplacement dans le texte du message marqué. Le reste du flux est une séquence d’attributs TNEF. Les attributs de message apparaissent en premier dans le flux TNEF, et les attributs de pièce jointe suivent. Les attributs qui appartiennent à une pièce jointe particulière sont regroupés, en commençant par l’attribut **attAttachRenddata** . 
  
La plupart des valeurs constantes utilisées dans les flux TNEF sont définies dans le TNEF. Fichier d’en-tête H. Notamment, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT** et tous les identificateurs d’attribut TNEF sont définis dans ce fichier. D’autres constantes ont les valeurs indiquées par leur interprétation à un compilateur de langage C. En règle générale, ces constantes sont utilisées pour donner les tailles de l’élément suivant. Par exemple, **sizeof(ULONG)** dans la définition d’un élément indique qu’un entier représentant la taille de l’entier long non signé suivant doit se produire à cet endroit dans le flux TNEF. 
  
Tous les entiers d’un flux TNEF sont stockés sous forme binaire little-endian, mais ils sont affichés en hexadécimal dans cette section. Les valeurs de somme de contrôle sont simplement des entiers non signés 16 bits qui sont la somme, modulo 65536, des octets de données auxquels la somme de contrôle s’applique. Toutes les longueurs d’attribut sont des entiers longs non signés, y compris tous les caractères null de fin.
  
La clé est un entier non différent de zéro, 16 bits non signé qui signifie la valeur initiale des clés de référence de pièce jointe. Les clés de référence de pièce jointe sont affectées à chaque pièce jointe de manière séquentielle, en commençant par la valeur initiale transmise à la fonction [OpenTnefStream](opentnefstream.md) par le fournisseur de services qui utilise TNEF. Le fournisseur de services doit générer une valeur initiale aléatoire pour la clé afin de réduire le risque que deux messages utilisent la même clé. 
  
L’implémentation TNEF utilise des identificateurs d’attributs pour mapper des attributs à leurs propriétés MAPI correspondantes. Un identificateur d’attribut est un entier non signé 32 bits composé de deux valeurs de mot. Le mot d’ordre élevé indique le type de données, tel que chaîne ou binaire, et le mot de bas niveau identifie l’attribut particulier. Les types de données dans le mot d’ordre élevé sont les suivants :
  
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
   
Les valeurs de mot de bas ordre pour chaque attribut sont définies dans le TNEF. Fichier d’en-tête H.
  

