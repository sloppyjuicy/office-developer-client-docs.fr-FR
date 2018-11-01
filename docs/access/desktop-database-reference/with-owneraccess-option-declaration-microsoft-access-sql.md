---
title: WITH OWNERACCESS OPTION, déclaration (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)
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
ms.openlocfilehash: 0ef07e29258035486a89e1b2cc19519d3f2f7c9f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889965"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>WITH OWNERACCESS OPTION, déclaration (Microsoft Access SQL)


**S’applique à**: Access 2013, Office 2013

Dans un environnement multi-utilisateurs doté d'un groupe de travail sécurisé, utilisez cette déclaration avec une requête pour octroyer à l'utilisateur exécutant la requête les mêmes autorisations que le propriétaire de la requête.

## <a name="syntax"></a>Syntaxe

*InstructionSQL* AVEC OWNERACCESS OPTION

## <a name="remarks"></a>Notes

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

