---
title: 'Chapitre 14 : Principes de base ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296464"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="5ea9f-102">Chapitre 14 : Principes de base ADO MD</span><span class="sxs-lookup"><span data-stu-id="5ea9f-102">Chapter 14: ADO MD fundamentals</span></span>

<span data-ttu-id="5ea9f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ea9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ea9f-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) permet d'accéder facilement aux données multidimensionnelles de langages tels que Microsoft Visual Basic, Microsoft Visual C++ et Microsoft Visual J++. ADO MD étend Microsoft ActiveX Data Objects (ADO) afin d'inclure des objets spécifiques à des données multidimensionnelles, tels que les objets [CubeDef](cubedef-object-ado-md.md) et [Cellset](cellset-object-ado-md.md). Avec ADO MD, vous pouvez parcourir un schéma multidimensionnel, exécuter une requête sur un cube et récupérer des résultats.</span><span class="sxs-lookup"><span data-stu-id="5ea9f-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="5ea9f-p102">À l'instar d'ADO, ADO MD utilise un fournisseur OLE DB sous-jacent pour accéder aux données. Pour utiliser ADO MD, le fournisseur doit être un fournisseur de données multidimensionnelles (MDP), tel qu'il est défini par OLE DB pour la spécification OLAP. Les fournisseurs de données multidimensionnelles présentent les données dans des vues multidimensionnelles, contrairement aux fournisseurs de données tabulaires (TDP), qui présentent les données dans des vues tabulaires. Consultez la documentation de votre fournisseur OLAP OLE DB pour des informations détaillées sur la syntaxe et le comportement spécifiques pris en charge par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5ea9f-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="5ea9f-111">Ce document suppose une connaissance pratique du langage de programmation Visual Basic et une connaissance générale d'ADO et d'OLAP.</span><span class="sxs-lookup"><span data-stu-id="5ea9f-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="5ea9f-112">Pour plus d’informations, voir le guide du [programmeur ADO](ado-programmer-s-guide.md) et la référence du programmeur OLE DB pour OLAP.</span><span class="sxs-lookup"><span data-stu-id="5ea9f-112">For more information, see the [ADO programmer's guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="5ea9f-113">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5ea9f-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="5ea9f-114">Vue d’ensemble des données et des schémas multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="5ea9f-114">Overview of multidimensional schemas and data</span></span>](overview-of-multidimensional-schemas-and-data.md)
- [<span data-ttu-id="5ea9f-115">Utilisation des données multidimensionnelles</span><span class="sxs-lookup"><span data-stu-id="5ea9f-115">Working with multidimensional data</span></span>](working-with-multidimensional-data.md)
- [<span data-ttu-id="5ea9f-116">Utilisation d'ADO avec ADO MD</span><span class="sxs-lookup"><span data-stu-id="5ea9f-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)
- [<span data-ttu-id="5ea9f-117">Programmation avec ADO MD</span><span class="sxs-lookup"><span data-stu-id="5ea9f-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
