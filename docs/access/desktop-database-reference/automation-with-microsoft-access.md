---
title: Automation avec Microsoft Access
TOCTitle: Automation with Microsoft Access
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bd0e230d2b4c31d497e913e8e1ccf4d2172402e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471102"
---
# <a name="automation-with-microsoft-access"></a>Automation avec Microsoft Access


**S’applique à**: Access 2013 | Office 2013

Microsoft Access est un composant COM qui prend en charge l'automation, autrefois appelée automation OLE. Microsoft Access prend en charge l'automation de deux manières. À partir de Microsoft Access, vous pouvez utiliser les objets fournis par une autre application. Microsoft Access fournit également ses objets à d'autres composants COM.

Vous pouvez utiliser le mot clé **New** ou la méthode **CreateObject** pour créer une nouvelle instance d'un composant. Vous pouvez utiliser la méthode **GetObject** pour affecter une variable à une instance existante d'un composant.

Dans Microsoft Access, vous pouvez définir une référence à la bibliothèque de types d'un composant pour améliorer les performances lorsque vous utilisez ce composant au moyen de l'automation. Microsoft Access contient également l'Explorateur d'objets, un outil qui vous permet d'afficher les objets de la bibliothèque de types d'un autre composant, ainsi que leurs méthodes et propriétés.

La bibliothèque de types Microsoft Access fournit des informations relatives aux objets Microsoft Access à d'autres composants. Vous pouvez [définir une référence](https://msdn.microsoft.com/library/ff194944\(v=office.15\)) à Microsoft Access bibliothèque à partir d’un composant de type et afficher ses objets dans l’Explorateur d’objets.

Si vous voulez manipuler des objets Microsoft Access au moyen de l'automation, vous devez créer une instance de l'objet **[Application](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** Microsoft Access. Par exemple, supposez que vous souhaitiez afficher des données provenant de Microsoft Excel dans un formulaire ou un état Microsoft Access. Pour démarrer Microsoft Access à partir de Microsoft Excel, vous pouvez utiliser le mot réservé **New** pour créer une instance de l'objet **Application** Microsoft Access. Vous pouvez également utiliser la méthode **CreateObject** pour créer une instance de l'objet **Application** Microsoft Access ou la méthode **GetObject** pour affecter une variable objet à une instance existante de Microsoft Access. Consultez la documentation de votre application pour déterminer la syntaxe qu'elle prend en charge.

Si, quand vous avez lancé une instance de Microsoft Access, vous voulez contrôler un objet Microsoft Access quelconque, vous devez ouvrir une base de données ou un projet (.adp) dans la fenêtre Microsoft Access à l'aide de la méthode **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))** ou **[NewCurrentDatabase](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** dans le cas d'une base de données, ou de la méthode **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))** ou **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** s'il 'agit d'un projet.

Si vous avez ouvert Microsoft Access en vue d'utiliser uniquement les objets d'accès aux données fournis par Microsoft DAO, vous ne devez dès lors pas ouvrir une base de données dans la fenêtre Microsoft Access. Vous pouvez utiliser la propriété **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** de l'objet **Application** Microsoft Access pour accéder aux objets de la bibliothèque d'objets de Microsoft 12.0 Access Database Engine Object Library lors d'une opération d'automation.

