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
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="e7803-102">WITH OWNERACCESS OPTION, déclaration (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e7803-102">WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="e7803-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7803-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7803-104">Dans un environnement multi-utilisateurs doté d'un groupe de travail sécurisé, utilisez cette déclaration avec une requête pour octroyer à l'utilisateur exécutant la requête les mêmes autorisations que le propriétaire de la requête.</span><span class="sxs-lookup"><span data-stu-id="e7803-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7803-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7803-105">Syntax</span></span>

<span data-ttu-id="e7803-106">*InstructionSQL* AVEC OWNERACCESS OPTION</span><span class="sxs-lookup"><span data-stu-id="e7803-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="e7803-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e7803-107">Remarks</span></span>

<span data-ttu-id="e7803-108">La déclaration WITH OWNERACCESS OPTION est facultative.</span><span class="sxs-lookup"><span data-stu-id="e7803-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="e7803-109">Dans l'exemple suivant, l'utilisateur a la possibilité de visualiser les informations relatives aux salaires (même si par ailleurs il n'a pas l'autorisation requise pour visualiser la table Payroll ), sous réserve que le propriétaire de la requête ait bien cette autorisation :</span><span class="sxs-lookup"><span data-stu-id="e7803-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="e7803-110">Si un utilisateur n'a pas l'autorisation de créer une table ou d'y ajouter des données, vous pouvez utiliser WITH OWNERACCESS OPTION pour permettre à cet utilisateur d'exécuter une requête Création de table ou une requête Ajout.</span><span class="sxs-lookup"><span data-stu-id="e7803-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="e7803-111">Si vous désirez appliquer les paramètres de sécurité du groupe de travail et les autorisations des utilisateurs, n'utilisez pas la déclaration WITH OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="e7803-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="e7803-p101">Cette option nécessite que vous ayez accès au fichier System.mdw associé à la base de données. Elle n'est utile que dans le contexte d'une configuration multi-utilisateur sécurisée.</span><span class="sxs-lookup"><span data-stu-id="e7803-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

