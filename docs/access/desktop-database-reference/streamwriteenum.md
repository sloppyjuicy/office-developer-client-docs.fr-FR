---
title: StreamWriteEnum (référence de base de données du bureau Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f58b5173a1208812a6eb9fd06b5f4a414de21ddd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470130"
---
# <a name="streamwriteenum"></a><span data-ttu-id="51d14-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="51d14-102">StreamWriteEnum</span></span>


<span data-ttu-id="51d14-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="51d14-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="51d14-104">Spécifie si un séparateur de ligne est ajouté à la chaîne écrite dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="51d14-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51d14-105">Constant</span><span class="sxs-lookup"><span data-stu-id="51d14-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="51d14-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="51d14-106">Value</span></span></p></th>
<th><p><span data-ttu-id="51d14-107">Description</span><span class="sxs-lookup"><span data-stu-id="51d14-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51d14-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="51d14-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="51d14-109">0</span><span class="sxs-lookup"><span data-stu-id="51d14-109">0</span></span></p></td>
<td><p><span data-ttu-id="51d14-p101">Par défaut. Écrit la chaîne de texte spécifiée (paramètre <em>Data</em>) dans l'objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="51d14-p101">Default. Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51d14-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="51d14-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="51d14-113">1</span><span class="sxs-lookup"><span data-stu-id="51d14-113">1</span></span></p></td>
<td><p><span data-ttu-id="51d14-p102">Écrit une chaîne de texte et un caractère de séparateur de ligne dans un objet <strong>Stream</strong>. Si la propriété <a href="lineseparator-property-ado.md">LineSeparator</a> n’est pas définie, une erreur d’exécution est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="51d14-p102">Writes a text string and a line separator character to a <strong>Stream</strong> object. If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51d14-116">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="51d14-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="51d14-117">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="51d14-117">These constants do not have ADO/WFC equivalents.</span></span>

