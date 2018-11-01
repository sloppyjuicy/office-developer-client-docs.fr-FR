---
title: Automation avec Microsoft Access
TOCTitle: Automation with Microsoft Access
description: Microsoft Access est un composant COM qui prend en charge l'automation, autrefois appelée automation OLE.
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5104ab19c5fab816040d7a5d56fa6f425658c245
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874250"
---
# <a name="automation-with-microsoft-access"></a>Automatisation avec Microsoft Access

**S’applique à**: Access 2013, Office 2013

Microsoft Access est un composant COM qui prend en charge l'automation, autrefois appelée automation OLE. Microsoft Access prend en charge l'automation de deux manières. À partir de Microsoft Access, vous pouvez utiliser les objets fournis par une autre application. Microsoft Access fournit également ses objets à d'autres composants COM.

Vous pouvez utiliser le mot clé **New** ou la méthode **CreateObject** pour créer une nouvelle instance d'un composant. Vous pouvez utiliser la méthode **GetObject** pour affecter une variable à une instance existante d'un composant.

Dans Microsoft Access, vous pouvez définir une référence à la bibliothèque de types d'un composant pour améliorer les performances lorsque vous utilisez ce composant au moyen de l'automation. Microsoft Access contient également l'Explorateur d'objets, un outil qui vous permet d'afficher les objets de la bibliothèque de types d'un autre composant, ainsi que leurs méthodes et propriétés.

La bibliothèque de types Microsoft Access fournit des informations relatives aux objets Microsoft Access à d'autres composants. Vous pouvez [définir une référence](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) à Microsoft Access bibliothèque à partir d’un composant de type et afficher ses objets dans l’Explorateur d’objets.

Si vous voulez manipuler des objets Microsoft Access au moyen de l'automation, vous devez créer une instance de l'objet **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** Microsoft Access. Par exemple, supposez que vous souhaitiez afficher des données provenant de Microsoft Excel dans un formulaire ou un état Microsoft Access. Pour démarrer Microsoft Access à partir de Microsoft Excel, vous pouvez utiliser le mot réservé **New** pour créer une instance de l'objet **Application** Microsoft Access. Vous pouvez également utiliser la méthode **CreateObject** pour créer une instance de l'objet **Application** Microsoft Access ou la méthode **GetObject** pour affecter une variable objet à une instance existante de Microsoft Access. Consultez la documentation de votre application pour déterminer la syntaxe qu'elle prend en charge.

Une fois que vous avez lancé une instance de Microsoft Access, si vous souhaitez contrôler tous les objets Microsoft Access, vous devez ouvrir une base de données ou un projet (.adp) dans la fenêtre Microsoft Access en utilisant **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** ou la **[NewCurrentDatabase ](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** méthode pour une base de données ou à l’aide **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** ou la méthode **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** pour un projet.

Si vous avez ouvert Microsoft Access uniquement comme moyen de l’aide de Data Access Objects fournis par Microsoft DAO, vous n’avez pas besoin d’ouvrir une base de données dans la fenêtre Microsoft Access. Vous pouvez utiliser la propriété **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** de l’objet Microsoft Access **Application** pour accéder aux objets dans la bibliothèque d’objets Microsoft Office 12.0 Access base de données de moteur pendant une opération Automation.

