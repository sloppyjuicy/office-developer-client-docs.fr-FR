---
title: LIKE (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut inclure des caractères réguliers et des caractères génériques. Pendant la correspondance de modèle, les caractères réguliers doivent correspondre exactement aux caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être en correspondance avec des fragments arbitraires de la chaîne de caractères. L’utilisation de caractères génériques rend l’opérateur LIKE plus flexible que l’utilisation des opérateurs de comparaison de chaînes = et !=.
ms.openlocfilehash: 0ad520b8bf9acd10134f73c016c5ddc984e9e51a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568228"
---
# <a name="like-access-custom-web-app"></a>LIKE (Application web personnalisée Access)

Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut inclure des caractères réguliers et des caractères génériques. Pendant la correspondance de modèle, les caractères réguliers doivent correspondre exactement aux caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être en correspondance avec des fragments arbitraires de la chaîne de caractères. L’utilisation de caractères génériques **rend l’opérateur LIKE** plus flexible que l’utilisation des opérateurs de comparaison de chaînes = et !=. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ] 
  
**L’opérateur LIKE** contient les arguments suivants 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Oui  <br/> |Expression valide.  <br/> |
| *Pattern*  <br/> |Oui  <br/> |Chaîne de caractères spécifique à rechercher dans  *Expression*  . Peut inclure des caractères génériques. Reportez-vous aux remarques pour obtenir la liste des caractères génériques valides.  <br/> |
| *EscapeChar*  <br/> |Non  <br/> |Caractère placé devant un caractère générique pour indiquer que le caractère générique doit être interprété comme un caractère normal et non comme un caractère générique.  *EscapeChar est*  une expression de caractère qui n’a pas de valeur par défaut et qui ne doit être évaluée qu’à un seul caractère.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant contient les caractères génériques valides pour être utilisés dans l’argument *Motif.* 
  
|**Caractère générique**|**Description**|**Exemple**|
|:-----|:-----|:-----|
|%  <br/> |Toute chaîne de zéro caractères ou plus.  <br/> | *WHERE title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.  <br/> |
|_ (trait de soulignement)  <br/> |Tout caractère unique.  <br/> | *WHERE au_fname LIKE '_ean'*  trouve tous les prénoms à quatre lettres qui se terminent par ean (Dean, Names, et ainsi de suite).  <br/> |
|[]  <br/> |Tout caractère unique dans la plage spécifiée ([a-f]) ou jeu ([abcdef]).  <br/> | *WHERE au_lname LIKE '[C-P]arsen'*  finds author last names ending with arsen and starting with any single character between C and P, for example Carsen, Principal, Karsen, and so on.  <br/> |
|[^]  <br/> |Tout caractère unique ne se trouve pas dans la plage spécifiée ([^a-f]) ou n’est pas définie ([^abcdef]).  <br/> | *WHERE au_lname LIKE 'de[^l]%'*  tous les noms d’auteur commençant par de et où la lettre suivante n’est pas l.  <br/> |
   
Lorsque vous effectuez des comparaisons de chaînes à l’aide de **LIKE,** tous les caractères de la chaîne de modèle sont significatifs. Cela inclut les espaces de début ou de fin. Si une comparaison dans une requête consiste à renvoyer toutes les lignes avec une chaîne **like** 'abc' (abc suivie d’un espace unique), une ligne dans laquelle la valeur de cette colonne est abc (abc sans espace) n’est pas renvoyée. Toutefois, les blancs de fin, dans l’expression à laquelle le modèle est indiqué, sont ignorés. Si une comparaison dans une requête consiste à renvoyer toutes les lignes avec la chaîne **LIKE** 'abc' (abc sans espace), toutes les lignes qui commencent par abc et ont zéro ou plusieurs vides de fin sont renvoyées. 
  
Si l’un des arguments n’est pas d’un type de données de chaîne, il est converti en type de données de chaîne, si possible.
  

