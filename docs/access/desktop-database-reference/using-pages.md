---
title: À l’aide de Pages (référence de base de données du bureau Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b25123698f39e602b59a2f5cd6bd9a2f0595addb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472292"
---
# <a name="using-pages"></a>Utilisation des pages


**S’applique à**: Access 2013 | Office 2013

Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l'objet **Recordset**. *Les pages* sont des groupes d’enregistrements dont la taille est égale à **la propriété PageSize** . Même si la dernière page est incomplète et que le nombre d'enregistrements qu'elle contient est inférieur à la valeur de **PageSize**, elle est considérée comme une page supplémentaire dans la valeur **PageCount**. Si l’objet **Recordset** ne prend pas en charge cette propriété, **PageCount** sera -1 pour indiquer que le **PageCount** est déterminé.

La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété **AbsolutePage** pour accéder au premier enregistrement d'une page donnée. Ceci s'avère utile dans les scénarios de serveurs Web, pour offrir aux utilisateurs la possibilité de passer d'une page de données à une autre et de consulter un certain nombre d'enregistrements à la fois.

Cette propriété peut être définie à tout moment et sa valeur sera utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.

Utilisez la propriété **AbsolutePage** pour identifier le numéro de la page de l'enregistrement actif. Ici encore, le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.

**AbsolutePage** utilise des nombres en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier de l'objet **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page donnée. Le nombre total de pages est obtenu à l'aide de la propriété **PageCount**.

