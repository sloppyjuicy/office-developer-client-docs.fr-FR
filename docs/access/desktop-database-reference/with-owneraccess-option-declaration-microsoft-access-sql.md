---
title: WITH OWNERACCESS OPTION, déclaration (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0882f143f13f6bd6d66c894f242a9cd50ebf9489
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302505"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>WITH OWNERACCESS OPTION, déclaration (Microsoft Access SQL)


**S’applique à** : Access 2013, Office 2013

Dans un environnement multi-utilisateurs doté d'un groupe de travail sécurisé, utilisez cette déclaration avec une requête pour octroyer à l'utilisateur exécutant la requête les mêmes autorisations que le propriétaire de la requête.

## <a name="syntax"></a>Syntaxe

*sqlstatement* WITH OWNERACCESS OPTION

## <a name="remarks"></a>Remarques

La déclaration WITH OWNERACCESS OPTION est facultative.

Dans l'exemple suivant, l'utilisateur a la possibilité de visualiser les informations relatives aux salaires (même si par ailleurs il n'a pas l'autorisation requise pour visualiser la table Payroll ), sous réserve que le propriétaire de la requête ait bien cette autorisation :

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Si un utilisateur n'a pas l'autorisation de créer une table ou d'y ajouter des données, vous pouvez utiliser WITH OWNERACCESS OPTION pour permettre à cet utilisateur d'exécuter une requête Création de table ou une requête Ajout.

Si vous désirez appliquer les paramètres de sécurité du groupe de travail et les autorisations des utilisateurs, n'utilisez pas la déclaration WITH OWNERACCESS OPTION.

Cette option nécessite que vous ayez accès au fichier System.mdw associé à la base de données. Elle n'est utile que dans le contexte d'une configuration multi-utilisateur sécurisée.

