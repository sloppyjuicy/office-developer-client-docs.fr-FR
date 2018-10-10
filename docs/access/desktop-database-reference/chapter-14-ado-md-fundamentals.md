---
title: "Chapitre 14 : Principes fondamentaux d'ADO MD"
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d595136c229234dfa0cb04a44fbe45f58cd79fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469997"
---
# <a name="chapter-14-ado-md-fundamentals"></a>Chapitre 14 : Principes fondamentaux d'ADO MD


**S’applique à**: Access 2013 | Office 2013

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) permet d'accéder facilement aux données multidimensionnelles de langages tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD étend Microsoft ActiveX Data Objects (ADO) afin d'inclure des objets spécifiques à des données multidimensionnelles, tels que les objets [CubeDef](cubedef-object-ado-md.md) et [Cellset](cellset-object-ado-md.md). Avec ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête sur un cube et récupérer des résultats.

À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Consultez la documentation de votre fournisseur OLAP OLE DB pour des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur.

Ce document suppose une connaissance pratique du langage de programmation Visual Basic et une connaissance générale d'ADO et d'OLAP. Pour plus d'informations, consultez [Guide du programmeur ADO](ado-programmer-s-guide.md) et « OLE DB for OLAP Programmer's Reference ». Pour plus d'informations générales sur ADO MD, consultez les rubriques suivantes :

  - [Présentation des schémas et données multidimensionnels](overview-of-multidimensional-schemas-and-data.md)

  - [Utilisation de données multidimensionnelles](working-with-multidimensional-data.md)

  - [Utilisation d'ADO avec ADO MD](using-ado-with-ado-md.md)

  - [Programmation avec ADO MD](programming-with-ado-md.md)

