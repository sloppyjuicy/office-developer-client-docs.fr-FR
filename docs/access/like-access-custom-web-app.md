---
title: LIKE (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut contenir des caractères normaux et des caractères génériques. Lors de la mise en correspondance des modèles, les caractères normaux doivent correspondre exactement aux caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être mis en correspondance avec des fragments arbitraires de la chaîne de caractères. L'utilisation de caractères génériques rend l'opérateur LIKE plus flexible que l'utilisation des opérateurs de comparaison de chaînes = et! =.
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311080"
---
# <a name="like-access-custom-web-app"></a>LIKE (application Web personnalisée Access)

Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut contenir des caractères normaux et des caractères génériques. Lors de la mise en correspondance des modèles, les caractères normaux doivent correspondre exactement aux caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être mis en correspondance avec des fragments arbitraires de la chaîne de caractères. L'utilisation de caractères génériques rend l'opérateur **Like** plus flexible que l'utilisation des opérateurs de comparaison de chaînes = et! =. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *Expression*  AUCUN **Comme** *Modèle*  [ESCAPE *EscapeChar* ] 
  
L'opérateur **Like** contient les arguments suivants: 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Oui  <br/> |Expression valide.  <br/> |
| *Pattern*  <br/> |Oui  <br/> |Chaîne de caractères spécifique à rechercher dans *expression* . Peut contenir des caractères génériques. RePortez-vous aux remarques pour obtenir la liste des caractères génériques valides.  <br/> |
| *EscapeChar*  <br/> |Non  <br/> |Caractère placé devant un caractère générique pour indiquer que le caractère générique doit être interprété comme un caractère normal et non comme un caractère générique.  *EscapeChar* est une expression de caractères qui n'a pas de valeur par défaut et doit correspondre à un seul caractère.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant contient les caractères génériques qui sont valides pour une utilisation dans l'argument *pattern* . 
  
|**Caractère générique**|**Description**|**Exemple**|
|:-----|:-----|:-----|
|%  <br/> |Toute chaîne de zéro ou plusieurs caractères.  <br/> | *Où title LIKE'% Computer% '* recherche tous les titres de livre avec le mot «Computer» n'importe où dans le titre du livre.  <br/> |
|_ (trait de soulignement)  <br/> |Tout caractère unique.  <br/> | *Où AU_FNAME like «_ean»* recherche tous les noms de la première lettre se terminant par EAN (Dean, Jean, etc.).  <br/> |
|[]  <br/> |Tout caractère compris dans la plage spécifiée ([a-f]) ou défini ([abcdef]).  <br/> | *Où au_lname like' [C-P] faible'* recherche les noms des auteurs dont le nom se termine par «faible» et en commençant par un caractère unique entre C et P, par exemple Carsen, Larsen, Karsen, etc.  <br/> |
|[^]  <br/> |Tout caractère qui ne se trouve pas dans la plage spécifiée ([^ a-f]) ou Set ([^ abcdef]).  <br/> | *Où au_lname like'de [^ l]% '* tous les noms de famille commençant par de et où la lettre suivante n'est pas l.  <br/> |
   
Lorsque vous effectuez des comparaisons de chaînes à l'aide de **Like**, tous les caractères de la chaîne de modèle sont significatifs. Cela inclut les espaces de début ou de fin. Si une comparaison dans une requête consiste à renvoyer toutes les lignes contenant une chaîne **Like** «ABC» (ABC suivi d'un seul espace), une ligne dont la valeur est ABC (ABC sans espace) n'est pas renvoyée. Toutefois, les espaces de fin, dans l'expression à laquelle le modèle est mis en correspondance, sont ignorés. Si une comparaison dans une requête consiste à renvoyer toutes les lignes contenant la chaîne **Like** «ABC» (ABC sans espace), toutes les lignes commençant par ABC et ayant zéro, un ou plusieurs espaces de fin sont renvoyés. 
  
Si l'un des arguments n'est pas un type de données String, il est converti en un type de données String, si cela est possible.
  

