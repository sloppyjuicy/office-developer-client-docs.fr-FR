---
title: Extensions Visual C++ pour ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302751"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="322a7-102">Extensions Visual C++ pour ADO</span><span class="sxs-lookup"><span data-stu-id="322a7-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="322a7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="322a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="322a7-104">La méthode préférée de programmation ADO avec Visual C++ consiste à utiliser la **\# directive** d’importation, comme expliqué dans [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span><span class="sxs-lookup"><span data-stu-id="322a7-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="322a7-105">Toutefois, les versions antérieures d’ADO sont livrées avec une autre méthode de programmation à l’aide de Visual C++ : les extensions Visual C++.</span><span class="sxs-lookup"><span data-stu-id="322a7-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="322a7-106">Cette section documente cette fonctionnalité pour les personnes qui doivent gérer du code Visual C++ Extensions, mais le nouveau code ADO doit être écrit à l’aide de \# **l’importation.**</span><span class="sxs-lookup"><span data-stu-id="322a7-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="322a7-p102">Une des tâches les plus fastidieuses que doivent entreprendre les programmeurs en Visual C++ pour récupérer les données avec ADO consiste à convertir les données retournées en tant que type VARIANT en données C++, puis à stocker les données converties dans une classe ou une structure. De plus, la récupération des données C++ par l'intermédiaire du type VARIANT nuit aux performances du système.</span><span class="sxs-lookup"><span data-stu-id="322a7-p102">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure. In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="322a7-p103">ADO fournit une interface qui prend en charge la récupération des données en types de données C/C++ natifs sans devoir passer par un type VARIANT ainsi que des macros de préprocesseur qui simplifient l'utilisation de l'interface. Le programmeur dispose ainsi d'un outil souple, performant et facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="322a7-p103">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface. The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="322a7-p104">Un scénario de client C/C++ classique consiste à lier un enregistrement d'un objet [Recordset](recordset-object-ado.md) à une structure ou une classe C/C++ contenant des types C/C++ natifs. Si un type VARIANT est utilisé, vous devez écrire du code pour convertir les données de type VARIANT en types C/C++ natifs. Les extensions Visual C++ pour ADO facilitent cette opération.</span><span class="sxs-lookup"><span data-stu-id="322a7-p104">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types. When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types. The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="322a7-114">Reportez-vous aux rubriques suivantes pour en savoir plus sur les extensions Visual C++ pour ADO.</span><span class="sxs-lookup"><span data-stu-id="322a7-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="322a7-115">Utilisation des extensions Visual C++</span><span class="sxs-lookup"><span data-stu-id="322a7-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="322a7-116">En-tête d'extensions Visual C++</span><span class="sxs-lookup"><span data-stu-id="322a7-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="322a7-117">Exemple ADO avec les extensions Visual C++</span><span class="sxs-lookup"><span data-stu-id="322a7-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

