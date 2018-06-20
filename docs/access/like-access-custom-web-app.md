---
title: COMME (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut inclure des caractères normaux et des caractères génériques. Au cours de critères spéciaux, caractères normaux doivent correspondre exactement les caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être associés à des portions aléatoires de la chaîne de caractères. Utilisation de caractères génériques rend l’opérateur LIKE plus flexible que la = et ! = opérateurs de comparaison de chaînes.
ms.openlocfilehash: d3224647c621b05a08bdc863939d0cccae214463
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781864"
---
# <a name="like-access-custom-web-app"></a>COMME (accès personnalisé web app)

Détermine si une chaîne de caractères spécifique correspond à un modèle spécifié. Un modèle peut inclure des caractères normaux et des caractères génériques. Au cours de critères spéciaux, caractères normaux doivent correspondre exactement les caractères spécifiés dans la chaîne de caractères. Toutefois, les caractères génériques peuvent être associés à des portions aléatoires de la chaîne de caractères. Utilisation de caractères génériques rend l’opérateur **LIKE** plus flexible que la = et ! = opérateurs de comparaison de chaînes. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *Expression*  [NOT] **Comme** *Motif*  [ESCAPE *dont* ] 
  
L’opérateur **LIKE** contient les arguments suivants 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Oui  <br/> |Une expression valide.  <br/> |
| *Motif*  <br/> |Oui  <br/> |La chaîne de caractères à rechercher dans *l’Expression* spécifique. Peut inclure des caractères génériques. Reportez-vous aux remarques pour obtenir la liste des caractères génériques valides.  <br/> |
| *Dont*  <br/> |Non  <br/> |Un caractère est placé devant le caractère générique pour indiquer que le caractère générique doit être interprété comme un caractère normal et non comme un caractère générique.  *Dont* est une expression de caractères qui n’a aucune valeur par défaut et doit correspondre à un seul caractère.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant contient les caractères génériques qui sont valides pour une utilisation dans l’argument *Pattern* . 
  
|**Caractère générique**|**Description**|**Exemple**|
|:-----|:-----|:-----|
|%  <br/> |Toute chaîne de zéro ou plusieurs caractères.  <br/> | *Où titre comme « ordinateur % »* recherche tous les titres des ouvrages avec le terme « computer » n’importe où dans le titre du livre.  <br/> |
|_ (trait de soulignement)  <br/> |Tout caractère unique.  <br/> | *WHERE au_fname LIKE '_ean'* trouve tous les prénoms de quatre lettres se terminant par ean (Olivier, Sean, etc.).  <br/> |
|[]  <br/> |N’importe quel caractère de la plage spécifiée ([a-f]) ou ensemble ([abcdef]).  <br/> | *WHERE au_lname LIKE '[C-P] arsen'* trouve créer des noms se terminant par « arsen » et commençant par n’importe quel caractère unique compris entre C et P, par exemple Carsen, Larsen, Karsen et ainsi de suite.  <br/> |
|[^]  <br/> |Tout caractère non au sein de la plage spécifiée ([^ a-f]) ou ([^ abcdef]).  <br/> | *WHERE au_lname LIKE ' Excel [^ l] %'* tous les noms commençant par de et dont la lettre suivante n’est pas l d’auteurs.  <br/> |
   
Lorsque vous effectuez des comparaisons de chaînes à l’aide de **comme**, tous les caractères de la chaîne de modèle sont conséquents. Cela inclut les espaces de début ou de fin. Si une comparaison dans une requête doit renvoyer toutes les lignes contenant une chaîne **LIKE** « abc » (abc suivi d’un seul espace), une ligne dans laquelle la valeur de cette colonne est (abc sans espace) n’est pas retournée. Toutefois, les espaces, dans l’expression à laquelle le modèle est mis en correspondance, sont ignorés. Si une comparaison dans une requête doit renvoyer toutes les lignes contenant **la chaîne** « abc » (abc sans espace), toutes les lignes qui commencent par abc et zéro ou plusieurs espaces de fin sont renvoyés. 
  
Si l’un des arguments n’est pas un chaîne du type de données, il est converti en un type de données string, s’il est possible.
  

