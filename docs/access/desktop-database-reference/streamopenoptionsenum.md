---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3998f41c1400a2870633f19228cbf73189e9527a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471224"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="c2f98-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="c2f98-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="c2f98-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2f98-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c2f98-p101">Spécifie les options pour l'ouverture d'un objet [Stream](stream-object-ado.md). Les valeurs peuvent être combinées avec une opération OR.</span><span class="sxs-lookup"><span data-stu-id="c2f98-p101">Specifies options for opening a [Stream](stream-object-ado.md) object. The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2f98-106">Constant</span><span class="sxs-lookup"><span data-stu-id="c2f98-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="c2f98-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2f98-107">Value</span></span></p></th>
<th><p><span data-ttu-id="c2f98-108">Description</span><span class="sxs-lookup"><span data-stu-id="c2f98-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f98-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="c2f98-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f98-110">1</span><span class="sxs-lookup"><span data-stu-id="c2f98-110">1</span></span></p></td>
<td><p><span data-ttu-id="c2f98-111">Ouvre l’objet <strong>Stream</strong> en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c2f98-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f98-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="c2f98-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f98-113">4</span><span class="sxs-lookup"><span data-stu-id="c2f98-113">4</span></span></p></td>
<td><p><span data-ttu-id="c2f98-p102">Identifie le contenu du paramètre <em>Source</em> en tant qu’objet <a href="record-object-ado.md">Record</a> déjà ouvert. L’action par défaut est de traiter <em>Source</em> comme une URL pointant directement sur un nœud d’un arbre. La chaîne de données associée à ce nœud est ouverte.</span><span class="sxs-lookup"><span data-stu-id="c2f98-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f98-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="c2f98-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f98-118">-1</span><span class="sxs-lookup"><span data-stu-id="c2f98-118">-1</span></span></p></td>
<td><p><span data-ttu-id="c2f98-p103">Par défaut. Spécifie l'ouverture de l'objet <strong>Stream</strong> avec des options par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2f98-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c2f98-121">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="c2f98-121">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c2f98-122">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="c2f98-122">These constants do not have ADO/WFC equivalents.</span></span>

