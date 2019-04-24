---
title: RefreshRecord, action de macro
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307076"
---
# <a name="refreshrecord-macro-action"></a>RefreshRecord, action de macro


**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **ActualiserEnregistrement** pour mettre à jour la source d'enregistrement sous-jacente de la feuille de données ou du formulaire actif de manière à refléter les modifications apportées aux enregistrements dans le jeu en cours.

## <a name="remarks"></a>Remarques

L'action **ActualiserEnregistrement** affiche uniquement les modifications apportées aux enregistrements dans le jeu actif. Étant donné que l'action **ActualiserEnregistrement** n'actualise pas réellement la base de données, le jeu actuel n'inclut pas les enregistrements qui ont été ajoutés et n'exclut pas les enregistrements qui ont été supprimés depuis la dernière actualisation de la base de données ; il n'exclut pas non plus les enregistrements qui ne répondent plus aux critères de la requête ou du filtre. Pour actualiser la base de données, utilisez la méthode **[Actualiser](requery-macro-action.md)**. Lorsque la source d'enregistrement pour un formulaire est actualisée, le jeu d'enregistrements actuel reflète exactement toutes les données de la source d'enregistrement.

Le comportement de cette action de macro varie selon que vous l'appelez dans une base de données cliente ou une base de données Web.

## <a name="client-database"></a>Base de données cliente

Dans une base de données cliente, vous pouvez utiliser l'action **ActualiserEnregistrement** pour mettre à jour la source d'enregistrement sous-jacente de la feuille de données ou du formulaire actif de façon à refléter les modifications apportées aux données dans le jeu actuel. Les modifications comprennent celles apportées par l'utilisateur actuel ou par d'autres utilisateurs dans un environnement multi-utilisateur. Elle équivaut à la méthode **[Actualiser](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**.

L'action de macro **ActualiserEnregistrement** effectue les opérations suivantes dans une base de données cliente :

1.  Elle met à jour la source d'enregistrement pour la feuille de données ou le formulaire actif de façon à refléter les modifications apportées aux lignes dans le jeu actuel. Pour les tables liées ODBC, elle extrait de la source de données les modifications apportées aux enregistrements dans le jeu actuel.

2.  Elle met à jour le jeu actuel de façon à refléter les modifications apportées. Si une ligne de la source d'enregistrement a été supprimée, elle est remplacée \#pour afficher la suppression.

3.  Actualise la feuille de données ou active pour afficher les enregistrements modifiés et \#les enregistrements supprimés dans le jeu actuel.

4.  Elle actualise tous les sous-formulaires et sous-états dans la feuille de données ou le formulaire actif.

## <a name="web-database"></a>Base de données Web

Dans une base de données Web, vous pouvez utiliser l'action **ActualiserEnregistrement** pour mettre à jour la source d'enregistrement sous-jacente de la feuille de données ou du formulaire actif de façon à refléter les modifications apportées aux enregistrements dans le jeu actuel. Les modifications comprennent celles apportées par l'utilisateur actuel ou par d'autres utilisateurs.

L'action de macro **ActualiserEnregistrement** effectue les opérations suivantes dans une base de données Web :

1.  Elle extrait les modifications à partir du serveur pour les tables de base dans le jeu actuel. Pour les tables liées ODBC, elle extrait de la source de données les modifications apportées aux enregistrements dans le jeu actuel.

2.  Elle met à jour le jeu actuel de façon à refléter les modifications apportées. Si une ligne du jeu actuel a été supprimée, elle est remplacée pour afficher \#la suppression.

3.  Actualise la feuille de données ou le formulaire actif pour afficher les enregistrements modifiés \#et les enregistrements supprimés dans le jeu actuel.

4.  Elle actualise tous les sous-formulaires et sous-états dans la feuille de données ou le formulaire actif.

