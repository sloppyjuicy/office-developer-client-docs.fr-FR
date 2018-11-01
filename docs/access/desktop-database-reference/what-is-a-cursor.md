---
title: Définition d'un curseur  (Référence de base de données du bureau access)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6dc2e38c7459fea46c33373447276d8643b4b0de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887375"
---
# <a name="what-is-a-cursor"></a>Qu’est-ce qu’un curseur ?


**S’applique à**: Access 2013, Office 2013

Les opérations effectuées dans une base de données relationnelle s'appliquent à l'ensemble d'un jeu de lignes. Le jeu de lignes renvoyé par une instruction SELECT comprend toutes les lignes qui répondent aux conditions de la clause WHERE de l'instruction. Ce jeu de lignes complet, retourné par l'instruction, est appelé « jeu de résultats ». Dans certaines applications, plus particulièrement les applications interactives et en ligne, le traitement global du jeu de résultats présente parfois des difficultés. Ces applications requièrent un mécanisme spécifique leur permettant de traiter une ligne ou un petit ensemble de lignes à la fois. Un curseur constitue une extension au jeux de résultats qui fournit ce mécanisme.

Un curseur est implémenté par une bibliothèque de curseurs. Une bibliothèque de curseurs est un logiciel implémenté la plupart du temps au sein d'un système de base de données ou d'une API d'accès aux données, qui permet la gestion des attributs de données renvoyées par une source de données (jeu de résultats). Ces attributs concernent la gestion de l'accès simultané, la position dans le jeu de résultats, le nombre de lignes renvoyées et la possibilité de défilement avant ou arrière dans le jeu de résultats.

Un curseur peut effectuer un suivi de la position dans le jeu de résultats, et permet d'effectuer un grand nombre d'opérations, ligne par ligne, dans un jeu de résultats, sans devoir nécessairement revenir à la table initiale. En d'autres termes, les curseurs sont conçus pour renvoyer un jeu de résultats basé sur des tables de bases de données. Le curseur est ainsi nommé car il indique la position active dans le jeu de résultats, à l'instar du curseur de l'écran de votre ordinateur.

Il est important de maîtriser le concept du curseur avant de passer aux spécificités de son utilisation dans ADO.

Les curseurs permettent d'effectuer les opérations suivantes :

  - Spécifier des positions sur des lignes spécifiques d'un jeu de résultats

  - Extraire une ligne ou un bloc de lignes en fonction de la position active dans le jeu de résultats

  - Modifier les données des lignes au niveau de la position active dans le jeu de résultats

  - Définir plusieurs niveaux de sensibilité des modifications apportées aux données par d'autres utilisateurs

Imaginons par exemple une application qui présente à un acheteur potentiel une liste de plusieurs produits. L'acheteur peut faire défiler la liste pour accéder aux informations et aux prix des produits, puis sélectionner un produit à acheter. Un défilement et une sélection supplémentaires s'appliquent au reste de la liste. Du point de vue de l'acheteur, les produits s'affichent un par un, mais l'application utilise un curseur de défilement vertical pour parcourir le jeu de résultats en amont et en aval.

Il est possible d'utiliser les curseurs de diverses façons :

  - sans aucune ligne ;

  - avec une partie ou l'ensemble des lignes d'une même table ;

  - avec une partie ou l'ensemble des lignes issues de tables jointes de façon logique ;

  - en mode lecture seule ou actualisable, au niveau du curseur ou au niveau du champ ;

  - en tant que curseur avant uniquement, ou avec défilement complet ;

  - avec le jeu de clés du curseur situé sur le serveur ;

  - sensibles aux modifications des tables sous-jacentes apportées par d'autres applications (appartenance, tri, insertion, mise à jour ou suppression) ;

  - installés sur le serveur ou sur le client.

Les curseurs en lecture seule permettent de parcourir le jeu de résultats, alors que les curseurs en lecture/écriture peuvent appliquer des mises à jour de lignes individuelles. Vous pouvez définir des curseurs complexes avec des jeux de clés qui repointent vers les lignes des tables de base de données. Certains curseurs sont en lecture seule en direction avant, et d'autres peuvent avancer et reculer et permettent une actualisation dynamique du jeu de résultats en fonction des modifications apportées à la base de données par d'autres applications.

Toutes les applications n'ont pas besoin de curseurs pour accéder aux données ou les mettre à jour. Certaines requêtes ne nécessitent pas de mise à jour directe de lignes à l'aide d'un curseur. Dans la mesure du possible, il ne faut utiliser les curseurs pour récupérer des données qu'en dernier recours et vous devez choisir le curseur dont l'impact est le plus limité possible. Lorsque vous créez un jeu de résultats à l'aide d'une procédure stockée, il n'est pas possible de mettre à jour le jeu de résultats en utilisant des méthodes de modification ou de mise à jour du curseur.

## <a name="concurrency"></a>Accès simultané

Dans certaines applications multi-utilisateurs, il est essentiel que l'utilisateur final bénéficie de données à jour. Un système de réservation d'une compagnie aérienne constitue un exemple classique de ce type de système. En effet, il se peut que plusieurs utilisateurs souhaitent réserver le même siège sur un vol donné (lequel représente donc un enregistrement unique). Dans ce cas, l'application doit pouvoir gérer les éventuelles opérations simultanées effectuées sur un même enregistrement.

L'accès simultané ne constitue pas toujours un élément aussi important dans toutes les applications. Pour certaines d'entre elles, les dépenses encourues pour conserver à tout moment des données à jour ne se justifient pas.

## <a name="position"></a>Position

Un curseur assure également le suivi de la position active dans un jeu de résultats. La position du curseur doit être considérée comme un pointeur vers l'enregistrement actif, à l'instar d'un index de tableau pointant vers un emplacement spécifique du tableau.

## <a name="scrollability"></a>Fonction de défilement

Le type de curseur utilisé par votre application affecte également la possibilité de déplacer vers l’avant et arrière dans les lignes d’un jeu de résultats ; Il est parfois appelée fonction de défilement. Possibilité de déplacer avant *et* arrière dans un jeu de résultats augmente la complexité du curseur et n’est donc plus coûteuse à implémenter. Pour cette raison, vous devez demander un curseur avec cette fonctionnalité uniquement lorsque cela est nécessaire.

