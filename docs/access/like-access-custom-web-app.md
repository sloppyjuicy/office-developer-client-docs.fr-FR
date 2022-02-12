---
title: LIKE (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut inclure des caractères réguliers et des caractères génériques. Pendant la correspondance de modèle, les caractères réguliers doivent correspondre exactement aux caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être en correspondance avec des fragments arbitraires de la chaîne de caractères. L’utilisation de caractères génériques rend l’opérateur LIKE plus flexible que l’utilisation des opérateurs de comparaison de chaînes = et !=.
ms.openlocfilehash: 5b2da376e781cec435a669c0644149e275eb594c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781680"
---
# <a name="like-access-custom-web-app"></a>LIKE (Application web personnalisée Access)

Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut inclure des caractères réguliers et des caractères génériques. Pendant la correspondance de modèle, les caractères réguliers doivent correspondre exactement aux caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être en correspondance avec des fragments arbitraires de la chaîne de caractères. L’utilisation de caractères génériques **rend l’opérateur LIKE** plus flexible que l’utilisation des opérateurs de comparaison de chaînes = et !=.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

 *Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE *EscapeChar* ]
  
**L’opérateur LIKE** contient les arguments suivants.

|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Oui  <br/> |Expression valide. |
| *Pattern*  <br/> |Oui  <br/> |Chaîne de caractères spécifique à rechercher dans *Expression*. Peut inclure des caractères génériques. Reportez-vous aux remarques pour obtenir la liste des caractères génériques valides. |
| *EscapeChar*  <br/> |Non  <br/> |Caractère placé devant un caractère générique pour indiquer que le caractère générique doit être interprété comme un caractère normal et non comme un caractère générique. *EscapeChar est* une expression de caractère qui n’a pas de valeur par défaut et qui ne doit être évaluée qu’à un seul caractère. |

## <a name="remarks"></a>Remarques

Le tableau suivant contient les caractères génériques valides pour une utilisation dans l’argument *Motif* . 
  
|**Caractère générique**|**Description**|**Exemple**|
|:-----|:-----|:-----|
|%  <br/> |Toute chaîne de zéro caractères ou plus. | *WHERE title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title. |
|_ (trait de soulignement)  <br/> |Tout caractère unique. | *WHERE au_fname LIKE '_ean'*  finds all four-letter first names that end with ean (Dean,Méra, and so on). |
|[]  <br/> |Tout caractère unique dans la plage spécifiée ([a-f]) ou jeu ([abcdef]). | *WHERE au_lname LIKE '[C-P]arsen'*  finds author last names ending with arsen and starting with any single character between C and P, for example Carsen, Principal, Karsen, and so on. |
|[^]  <br/> |Tout caractère unique ne se trouve pas dans la plage spécifiée ([^a-f]) ou n’est pas définie ([^abcdef]). | *WHERE au_lname LIKE 'de[^l]%'*  tous les noms d’auteur commençant par de et où la lettre suivante n’est pas l. |

Lorsque vous effectuez des comparaisons de chaînes à l’aide de **LIKE**, tous les caractères de la chaîne de modèle sont significatifs. Cela inclut les espaces de début ou de fin. Si une comparaison dans une requête consiste à renvoyer toutes les lignes avec une chaîne **LIKE** 'abc' (abc suivie d’un espace unique), une ligne dans laquelle la valeur de cette colonne est abc (abc sans espace) n’est pas renvoyée. Toutefois, les blancs de fin, dans l’expression à laquelle le modèle est indiqué, sont ignorés. Si une comparaison dans une requête consiste à renvoyer toutes les lignes avec la chaîne **LIKE** 'abc' (abc sans espace), toutes les lignes qui commencent par abc et ont zéro ou plusieurs vides de fin sont renvoyées.
  
Si l’un des arguments n’est pas d’un type de données de chaîne, il est converti en type de données de chaîne, si possible.
  