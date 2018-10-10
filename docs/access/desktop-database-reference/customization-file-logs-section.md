---
title: Section Logs du fichier de personnalisation
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471869"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="a7891-102">Section Logs du fichier de personnalisation</span><span class="sxs-lookup"><span data-stu-id="a7891-102">Customization File Logs Section</span></span>

<span data-ttu-id="a7891-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7891-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a7891-104">La section **logs** contient une entrée de fichier journal qui indique le nom du fichier qui enregistre les erreurs au cours du fonctionnement de l'objet **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="a7891-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7891-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7891-105">Syntax</span></span>

<span data-ttu-id="a7891-106">Une entrée de fichier journal a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="a7891-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7891-107">Partie</span><span class="sxs-lookup"><span data-stu-id="a7891-107">Part</span></span></p></th>
<th><p><span data-ttu-id="a7891-108">Description</span><span class="sxs-lookup"><span data-stu-id="a7891-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7891-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="a7891-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="a7891-110">Chaîne littéral qui indique qu'il s'agit d'une entrée de fichier journal.</span><span class="sxs-lookup"><span data-stu-id="a7891-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7891-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="a7891-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="a7891-p101">Chemin d'accès complet et nom du fichier. Le nom de fichier habituel est <strong>c:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7891-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7891-114">Le fichier journal contient le nom de l'utilisateur, HRESULT, la date et l'heure de chaque erreur.</span><span class="sxs-lookup"><span data-stu-id="a7891-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

