---
title: Utilisation de données multidimensionnelles
TOCTitle: Working with Multidimensional Data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7aba6eda9abc84c6f34442f828fe802c4b016653
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871989"
---
# <a name="working-with-multidimensional-data"></a>Utilisation de données multidimensionnelles


**S’applique à**: Access 2013, Office 2013

Un *ensemble de cellules* est le résultat d’une requête sur des données multidimensionnelles. Il est constitué d'une collection d'axes, quatre au maximum et deux ou trois en règle générale. Un *axe* est une collection de membres d’une ou plusieurs dimensions, qui permet de rechercher ou de filtrer des valeurs spécifiques dans un cube.

Une *position* est un point le long d’un axe. Pour un axe comprenant une seule dimension, ces positions constituent un sous-ensemble des membres de la dimension. Si un axe comprend plusieurs dimensions, chaque position est une entité composée, qui comprend les éléments *n* où *n* est le nombre de dimensions orientées le long de cet axe. Chaque partie de la position est un membre d'une dimension constitutive.

Par exemple, si les dimensions Géographie et Produit d'un cube contenant des données de ventes sont orientées le long de l'axe des x d'un ensemble de cellules, une position le long de cet axe peut contenir les membres « USA » et « Computers ». Dans cet exemple, les membres de chaque dimension doivent être orientés le long de l'axe des x pour y déterminer une position.

Une *cellule* est un objet placé à l’intersection des coordonnées des axes. Chaque cellule renferme plusieurs informations, notamment les données elles-mêmes, une chaîne mise en forme (la forme affichable des données de la cellule) et la valeur ordinale de la cellule. (Chaque cellule est une valeur ordinale unique de l'ensemble de cellules. La valeur ordinale de la première cellule de l'ensemble est zéro, tandis que celle de la cellule la plus à gauche de la deuxième ligne d'un ensemble de cellules contenant huit colonnes serait huit.)

Par exemple, un cube contient les six dimensions suivantes (notez que ce schéma de cube est légèrement différent de celui donné dans la rubrique [Présentation des schémas et données multidimensionnels](overview-of-multidimensional-schemas-and-data.md)) :

  - Vendeur

  - Géographie (hiérarchie naturelle)  Continents, Pays, États, etc.

  - Trimestres  Trimestres, Mois, Jours

  - Années

  - Mesures  Ventes, ChangementPourcentage, VentesBudget

  - Produits


> [!NOTE]
> <P>[!REMARQUE] Les valeurs de cellule de l'exemple peuvent être affichées sous forme de paires classées de valeurs ordinales de position sur les axes où le premier chiffre représente la position sur l'axe des x et le second la position sur l'axe des y.</P>



Cet ensemble de cellules présente les caractéristiques suivantes :

  - Dimensions des axes : Trimestres, Vendeur, Géographie

  - Dimensions de filtrage : Mesures, Années, Produits

  - Deux axes : COLONNE (x ou Axe 0) et LIGNE (y ou Axe 1)

  - axe des x : deux dimensions imbriquées, Vendeur et Géographie

  - axe des y : dimension Trimestres

L'axe des x comprend deux dimensions imbriquées : Vendeur et Géographie. Quatre membres de la dimension Géographie sont sélectionnés : Seattle, Boston, USA-South et Japan. Deux membres de la dimension Vendeur sont sélectionnés : Valentine et Nash. Ceci produit un total de huit positions sur cet axe (8 = 4\*2).

Chaque coordonnée est représentée sous la forme d'une position avec deux membres  une pour la dimension Vendeur et une autre pour la dimension Géographie :

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

L'axe des y ne comprend qu'une seule dimension, regroupant les huit positions suivantes :

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

Les ensembles de cellules, les cellules, les axes et les positions sont tous représentés par leurs objets ADO MD correspondants : [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) et [Position](position-object-ado-md.md).

