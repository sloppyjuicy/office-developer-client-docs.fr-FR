---
title: Extensions Visual C++ pour ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7d3a5e876dd98e26c2eb9169a21a8dcd5e532e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471337"
---
# <a name="visual-c-extensions-for-ado"></a>Extensions Visual C++ pour ADO


**S’applique à**: Access 2013 | Office 2013

À l’aide de la méthode préférée de programmation ADO avec Visual C++ est la ** \#importer** directive, comme indiqué dans la [Programmation ADO Visual C++](visual-c-ado-programming.md). Toutefois, les versions précédentes d’ADO fourni avec une autre méthode de programmation à l’aide de Visual C++ : les Extensions Visual C++. Cette section décrit cette fonctionnalité pour les utilisateurs qui doivent conserver Extensions Visual C++, mais le nouveau code ADO doit être écrite à l’aide de \# **Importer**.

Une des tâches les plus fastidieuses que doivent entreprendre les programmeurs en Visual C++ pour récupérer les données avec ADO consiste à convertir les données retournées en tant que type VARIANT en données C++, puis à stocker les données converties dans une classe ou une structure. De plus, la récupération des données C++ par l'intermédiaire du type VARIANT nuit aux performances du système.

ADO fournit une interface qui prend en charge la récupération des données en types de données C/C++ natifs sans devoir passer par un type VARIANT ainsi que des macros de préprocesseur qui simplifient l'utilisation de l'interface. Le programmeur dispose ainsi d'un outil souple, performant et facile à utiliser.

Un scénario de client C/C++ classique consiste à lier un enregistrement d'un objet [Recordset](recordset-object-ado.md) à une structure ou une classe C/C++ contenant des types C/C++ natifs. Si un type VARIANT est utilisé, vous devez écrire du code pour convertir les données de type VARIANT en types C/C++ natifs. Les extensions Visual C++ pour ADO facilitent cette opération.

Reportez-vous aux rubriques suivantes pour en savoir plus sur les extensions Visual C++ pour ADO.

  - [Utilisation des extensions Visual C++](using-visual-c-extensions.md)

  - [En-tête d'extensions Visual C++](visual-c-extensions-header.md)

  - [Exemple ADO avec les extensions Visual C++](visual-c-extensions-example.md)

