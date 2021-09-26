---
title: À propos des opérateurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251824
ms.localizationpriority: medium
ms.assetid: 43128ea2-c0d9-c45f-31e6-768a80ae59b2
description: Vous pouvez utiliser des opérateurs dans des formules pour effectuer des opérations arithmétiques (addition, soustraction, multiplication, etc.) ou des comparaisons logiques (supérieur à, inférieur à, égal à, etc.). Vous pouvez également définir l’ordre d’évaluation dans une formule en plaçant les expressions entre parenthèses. Utilisez l’opérateur & pour combiner (concaténer) des chaînes de caractères.
ms.openlocfilehash: 81829e04445652ce45b3b1ff92339b2090c2fcb9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619175"
---
# <a name="about-operators"></a>À propos des opérateurs

Vous pouvez utiliser des opérateurs dans des formules pour effectuer des opérations arithmétiques (addition, soustraction, multiplication, etc.) ou des comparaisons logiques (supérieur à, inférieur à, égal à, etc.). Vous pouvez également définir l’ordre d’évaluation dans une formule en plaçant les expressions entre parenthèses. Utilisez l’opérateur & pour combiner (concaténer) des chaînes de caractères.
  
Microsoft Visio tente automatiquement de convertir les types de données lorsqu’une opération ou une fonction nécessite un type particulier de données. Par exemple, l’opérateur de multiplication exige des arguments numériques et l’opérateur & (concaténation de chaînes) des arguments chaîne. Si l’argument ne peut pas être converti dans le type de données requis, une valeur par défaut est fournie. Cette valeur par défaut est l’équivalent dans un type de variable d’un élément vide : zéro pour les nombres, FALSE pour les valeurs booléennes, "" pour les chaînes, etc.
  
Le tableau ci-dessous montre des exemples d’expressions avec leurs résultats.
  
|**Expression**|**Résultat**|**Description**|
|:-----|:-----|:-----|
| 2 \* 5 &amp; »  <br/> | "10 cents"  <br/> | L’opérateur (concatenation de chaîne) requiert des arguments de chaîne, de sorte que le résultat numérique de 2 5 est automatiquement converti en chaîne &amp; \* « 10 ».  <br/> |
| 5 \* « 2 »  <br/> | 10  <br/> | L’opérateur (multiplication) requiert des arguments numériques, de sorte que la chaîne « 2 » est automatiquement convertie en nombre \* équivalent 2.  <br/> |
| 5 \* « sous »  <br/> | 0  <br/> | L’opérateur (multiplication) requiert des arguments numériques, donc, étant donné que la chaîne « er » ne peut pas être convertie en nombre, zéro est utilisé comme équivalent \* numérique.  <br/> |
   
## <a name="arithmetic-operators"></a>Opérateurs arithmétiques

Les opérateurs arithmétiques réalisent des opérations sur des nombres. Les opérateurs + et - peuvent être utilisés comme opérateurs unaires pour définir le signe d’un nombre. L’opérateur % est aussi un opérateur unaire qui identifie le nombre comme pourcentage.
  
|**Opérateur**|**Action**|**Exemple**|**Résultat**|
|:-----|:-----|:-----|:-----|
| +  <br/> | Positif  <br/> | +37  <br/> | 37  <br/> |
| -  <br/> | Négatif  <br/> | -37  <br/> | -37  <br/> |
| %  <br/> | Pourcentage  <br/> | 37 %  <br/> | .37  <br/> |
| ^  <br/> | Exponentiation  <br/> | 5 ^ 2  <br/> | 25  <br/> |
| \*  <br/> | Multiplication  <br/> | 5 \* 2  <br/> | 10  <br/> |
| /  <br/> | Division  <br/> | 5/2  <br/> | 2,5  <br/> |
| +  <br/> | Ajout  <br/> | 5 + 2  <br/> | 7   <br/> |
| -  <br/> | Soustraction  <br/> | 5 - 2  <br/> | 3  <br/> |
   
## <a name="comparison-operators"></a>Opérateurs de comparaison

Les opérateurs de comparaison sont utilisés pour construire des expressions logiques. Une expression logique renvoie FALSE ou TRUE.
  
|**Opérateur**|**Solution alternative**|**Action**|**Exemple**|**Résultat**|
|:-----|:-----|:-----|:-----|:-----|
| \>  <br/> | _GT_  <br/> | Supérieur à  <br/> | 5 \> 2  <br/> | TRUE  <br/> |
| \<  <br/> | _LT_  <br/> | Inférieur à  <br/> | 5 \< 2  <br/> | FALSE  <br/> |
| \>=  <br/> | _GE_  <br/> | Supérieur ou égal à  <br/> | 5 \> = 2  <br/> | TRUE  <br/> |
| \<=  <br/> | _LE_  <br/> | Inférieur ou égal à  <br/> | 5 \<= 2  <br/> | FALSE  <br/> |
| =  <br/> | _EQ_  <br/> | Égal à  <br/> | 5 = 2  <br/> | FALSE  <br/> |
| \<\>  <br/> | _NE_  <br/> | Différent de  <br/> | 5 \<\> 2  <br/> | TRUE  <br/> |
   
Les opérateurs de comparaison symboliques ( et ainsi de suite) sont \> le meilleur choix pour la plupart des \< comparaisons. Les opérateurs alternatifs _(GT,_ _LT,_ etc.) effectuent une comparaison exacte avec les 15 chiffres complets de précision que Visio utilise pour stocker des valeurs en interne.
  
Lorsque vous comparez des valeurs arrondies ou calculées à l’aide de ces opérateurs de remplacement, la valeur FALSE peut être renvoyée, alors que dans la pratique, l’expression devrait renvoyer TRUE.
  
Lorsque vous comparez des chaînes de texte, elles sont d’abord converties en valeurs numériques. Les chaînes de texte qui ne peuvent être converties renvoient une valeur zéro. De ce fait, les comparaisons varient et sont susceptibles de ne pas toujours produire les résultats escomptés. Pour effectuer une comparaison standard de chaînes, utilisez la fonction STRSAME ou STRSAMEEX.
  
## <a name="order-of-evaluation"></a>Ordre d’évaluation

Lorsqu’une formule contient plusieurs expressions, elles sont évaluées dans l’ordre des opérations à réaliser. Le tableau ci-dessous indique l’ordre d’évaluation des opérateurs dans Visio.
  
|**Order**|**Action**|**Opérateur**|
|:-----|:-----|:-----|
|Premier  <br/> |Positif  <br/> |+ (unaire)  <br/> |
||Negative  <br/> |- (unaire)  <br/> |
||Pourcentage  <br/> |% (unaire)  <br/> |
|Deuxième  <br/> |Exponentiation  <br/> |^  <br/> |
|Troisième  <br/> |Multiplication  <br/> |\*  <br/> |
||Division  <br/> |/  <br/> |
|Quatrième  <br/> |Addition  <br/> |+  <br/> |
||Soustraction  <br/> |-  <br/> |
|Cinquième  <br/> |Concaténation de chaînes  <br/> |&amp;  <br/> |
|Sixième  <br/> |Supérieur à  <br/> |\> ou GT  <br/> |
||Supérieur ou égal à  <br/> |\>= ou GE  <br/> |
||Inférieur à  <br/> |\< or LT  <br/> |
||Inférieur ou égal à  <br/> |\<= or LE  <br/> |
|Septième  <br/> |Égal  <br/> |= ou EQ  <br/> |
||Différent de  <br/> |\<\> ou NE  <br/> |
   
Vous pouvez modifier l’ordre d’évaluation en mettant des expressions entre parenthèses. Visio évalue d’abord les expressions entre parenthèses, de la gauche vers la droite. Exemple :
  
4 + 5 \* 6 = 4 + 30 = 34
  
(4 + 5) \* 6 = 9 \* 6 = 54
  
Si les expressions entre parenthèses sont imbriquées, Visio évalue en premier l’expression la plus profonde.
  
## <a name="ampersand-operator"></a>Opérateur &

L’opérateur & renvoie une nouvelle chaîne de caractères. Vous pouvez créer des mots ou des locutions composés à l’aide de cet opérateur. Utilisez la syntaxe suivante :
  
« string1 » &amp; « string2 »
  
 **Exemple**
  
« dog " &amp; « house » renvoie « doghouse »
  

