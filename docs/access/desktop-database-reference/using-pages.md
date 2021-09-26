---
title: Utilisation de pages (référence de base de données de bureau Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a2aab91f10341b6fbe2ccef74c6df3f2b9217ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631635"
---
# <a name="using-pages"></a>Utilisation de pages


**S’applique à** : Access 2013, Office 2013

Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l’objet **Recordset**. Les *Pages* sont des groupes d’enregistrements dont la taille est égale à la valeur de la propriété **PageSize**. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.

La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété **AbsolutePage** pour accéder au premier enregistrement d'une page donnée. Ceci s'avère utile dans les scénarios de serveurs Web, pour offrir aux utilisateurs la possibilité de passer d'une page de données à une autre et de consulter un certain nombre d'enregistrements à la fois.

Cette propriété peut être définie à tout moment et sa valeur sera utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.

Utilisez la propriété **AbsolutePage** pour identifier le numéro de la page de l'enregistrement actif. Ici encore, le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.

**AbsolutePage** utilise des nombres en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier de l'objet **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page donnée. Le nombre total de pages est obtenu à l'aide de la propriété **PageCount**.

