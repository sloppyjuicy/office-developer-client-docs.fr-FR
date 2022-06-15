---
title: Automatisation avec Microsoft Access
TOCTitle: Automation with Microsoft Access
description: Microsoft Access est un composant COM qui prend en charge Automation, précédemment appelé OLE Automation.
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: a4484ccebb3eff532a669ff3d89e895bb22840d6
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083821"
---
# <a name="automation-with-microsoft-access"></a>Automation avec Microsoft Access

**S’applique à** : Access 2013, Office 2013

Microsoft Access est un composant COM qui prend en charge Automation, anciennement appelé OLE Automation. Microsoft Access prend en charge l’automatisation de deux façons. À partir de Microsoft Access, vous pouvez travailler avec des objets fournis par un autre composant. Microsoft Access fournit également ses objets à d’autres composants COM.

Vous pouvez utiliser la **nouveau** mot clé ou le **CreateObject** méthode pour créer une nouvelle instance d’un composant. Vous pouvez utiliser la **GetObject** méthode pour attribuer une variable sur une instance d’un composant existante.

Dans Microsoft Access, vous pouvez définir une référence à la bibliothèque de types de composant pour améliorer les performances lorsque vous travaillez avec ce composant via Automation. Microsoft Access inclut également l’Explorateur d’objets, un outil qui vous permet d’afficher des objets dans une autre bibliothèque de type composant, ainsi que leurs méthodes et propriétés.

La bibliothèque de types Microsoft Access fournit des informations relatives aux objets Microsoft Access à d'autres composants. Vous pouvez [définir une référence](/office/vba/access/Concepts/Settings/set-references-to-type-libraries) à la bibliothèque de types Microsoft Access à partir d'un composant et afficher ses objets dans l'Explorateur d'objets.

Pour utiliser les objets Microsoft Access via Automation, vous devez créer une instance de Microsoft Access **[Application](/office/vba/api/Access.Application)** objet. Par exemple, supposons que vous voulez afficher des données à partir de Microsoft Excel dans un formulaire dans Microsoft Access ou un état. Pour lancer Microsoft Access à partir de Microsoft Excel, vous pouvez utiliser la **nouveau** mot clé pour créer une instance de Microsoft Access **Application** objet. Vous pouvez également utiliser le **CreateObject** méthode pour créer une nouvelle instance de Microsoft Access **Application** objet, ou vous pouvez utiliser la **GetObject** méthode permettant de pointez une variable d’objet sur une instance de Microsoft Access existante. Consultez la documentation de votre composant pour déterminer la syntaxe Il prend en charge.

Si, après avoir lancé une instance de Microsoft Access, vous voulez contrôler un objet Microsoft Access quelconque, vous devez ouvrir une base de données ou un projet (.adp) dans la fenêtre Microsoft Access à l’aide de la méthode **[OpenCurrentDatabase](/office/vba/api/Access.Application.OpenCurrentDatabase)** ou **[NewCurrentDatabase](/office/vba/api/Access.Application.NewCurrentDatabase)** s’il s’agit d’une base de données, ou de la méthode **[OpenAccessProject](/office/vba/api/Access.Application.OpenAccessProject)** ou **[NewAccessProject](/office/vba/api/Access.Application.NewAccessProject)** s’il ’agit d’un projet.

Si vous avez ouvert Microsoft Access en vue d'utiliser uniquement les objets d'accès aux données fournis par Microsoft DAO, vous ne devez dès lors pas ouvrir une base de données dans la fenêtre Microsoft Access. Vous pouvez utiliser la propriété **[DBEngine](/office/vba/api/Access.Application.DBEngine)** de l'objet **Application** Microsoft Access pour accéder aux objets de la bibliothèque d'objets de Microsoft Office 12.0 Access Database Engine Object Library lors d'une opération d'automation.
