---
title: Jeux d'enregistrements hiérarchiques et filtrés persistants
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 931345aff0cd3d8c9b10c53073e640b3cfdd5de5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889713"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="8ac6c-102">Jeux d'enregistrements hiérarchiques et filtrés persistants</span><span class="sxs-lookup"><span data-stu-id="8ac6c-102">Persisting Filtered and Hierarchical Recordsets</span></span>


<span data-ttu-id="8ac6c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ac6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ac6c-p101">Si la propriété [Filter](filter-property-ado.md) est activée pour le **jeu d'enregistrements**, seules les lignes accessibles via le filtre sont sauvegardées. Si le **jeu d'enregistrements** est hiérarchique, le **jeu d'enregistrements** enfant et ses enfants sont sauvegardés, y compris le **jeu d'enregistrements** parent. Si la méthode **Save** d'un **jeu d'enregistrements** enfant est invoquée, l'enfant et tous ces enfants sont enregistrés, mais pas le parent. Pour en savoir plus sur les **jeux d'enregistrements** hiérarchiques, reportez-vous au [Chapitre 9 : Mise en forme des données](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="8ac6c-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="8ac6c-p102">[!REMARQUE] Certaines restrictions s'appliquent lors de la sauvegarde de <STRONG>jeux d'enregistrements</STRONG> hiérarchiques (formes de données) au format XML. Pour en savoir plus, reportez-vous à la rubrique <A href="hierarchical-recordsets-in-xml.md">Jeux d'enregistrements hiérarchiques dans XML</A>.</span><span class="sxs-lookup"><span data-stu-id="8ac6c-p102">Some limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. For more information, see <A href="hierarchical-recordsets-in-xml.md">Hierarchical Recordsets in XML</A>.</span></span></P>


