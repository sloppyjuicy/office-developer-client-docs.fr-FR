---
title: Ajout de données à un recordset
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701395"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="78321-102">Ajout de données à un recordset</span><span class="sxs-lookup"><span data-stu-id="78321-102">Adding data to a Recordset</span></span>

<span data-ttu-id="78321-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78321-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78321-p101">Le **jeu d'enregistrements** est certainement l'objet ADO le plus utilisé. Dans ADO, un **jeu d'enregistrements** peut se définir comme une combinaison d'un jeu de résultats provenant d'une source de données et des comportements de curseurs associés. Vous pouvez ainsi mettre des données dans un **jeu d'enregistrements** et utiliser les méthodes et propriétés **Recordset** pour parcourir les lignes de données, afficher les valeurs de ces lignes ou encore manipuler le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="78321-p101">The **Recordset** is probably the most used of the ADO objects. In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors. Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="78321-p102">Cette section s'intéresse plus particulièrement à l'ajout de données au **jeu d'enregistrements**. Pour en savoir plus sur la manière de parcourir ou mettre à jour les données, reportez-vous au [Chapitre 4 : Modification des données](chapter-4-editing-data.md) et au [Chapitre 5 : Mise à jour et conservation des données](chapter-5-updating-and-persisting-data.md). Les capacités avancées d'un objet **Command** ne sont pas toujours nécessaires pour ajouter votre jeu de résultats à un **jeu d'enregistrements**. Bien souvent, vous pouvez exécuter votre commande en définissant la propriété **Source** du **jeu d'enregistrements** ou en transférant une chaîne de commande à la méthode **Open** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="78321-p102">This section will focus on adding data to the **Recordset**. For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md). You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**. Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="78321-p103">Il existe différentes façons d'ajouter les données de votre source de données à un **jeu d'enregistrements**. La technique utilisée dépend des besoins de votre application et des capacités de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="78321-p103">There are a variety of ways to add data from your data source to a **Recordset**. The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

