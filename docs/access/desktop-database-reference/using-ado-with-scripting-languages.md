---
title: Utilisation d'ADO avec des langages de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312039"
---
# <a name="using-ado-with-scripting-languages"></a>Utilisation d’ADO avec langages de script


**S’applique à** : Access 2013, Office 2013

Dans un environnement de script, ADO vous permet d'exposer des données via un script côté serveur. Dans ce scénario, ADO, le fournisseur de la base de données OLE sous-jacent qu'il utilise, ainsi que tous les autres composants requis pour référencer un magasin de données particulier sont installés sur un serveur exécutant IIS (Internet Information Services). Avec ASP (Active Server Pages), ADO est un composant référencé dans un script qui peut générer, par exemple, du contenu HTML. Ce contenu HTML peut être transmis via HTTP à un navigateur web client. Grâce à l’utilisation de scripts, la page web peut renvoyer des actions au script côté serveur, ce qui vous permet de mettre à jour, de parcourir ou d’afficher des données spécifiques.

## <a name="odbc-data-sources"></a>Sources de données ODBC

La source de données ODBC, lorsqu'elle est utilisée, constitue une différence notable entre les codes ADO avec et sans script. Dans les applications sans script, vous pouvez créer un DSN utilisateur dans l'administrateur de la source de données ODBC. Pour les scripts exécutés sous IIS, vous devez créer un DSN système, sans quoi, vos scripts ne reconnaîtront pas la source de données que vous avez créée. Ceci vaut pour toutes les applications de script ADO qui utilisent le fournisseur de base de données Microsoft OLE pour la source de données ODBC via Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Référence à la bibliothèque ADO

N/A avec des langages de script

## <a name="handling-events"></a>Gestion d'événements

N/A avec des langages de script

Les rubriques suivantes contiennent des informations détaillées sur l'utilisation d'ADO avec des langages de script :

- [Programmation ADO en JScript](jscript-ado-programming.md)

- [Programmation ADO en VBScript](vbscript-ado-programming.md)
