---
title: Section des journaux du fichier de personnalisation
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295148"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="64f88-102">Section des journaux du fichier de personnalisation</span><span class="sxs-lookup"><span data-stu-id="64f88-102">Customization File Logs section</span></span>

<span data-ttu-id="64f88-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64f88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64f88-104">La section **logs** contient une entrée de fichier journal qui indique le nom du fichier qui enregistre les erreurs au cours du fonctionnement de l'objet **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="64f88-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f88-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64f88-105">Syntax</span></span>

<span data-ttu-id="64f88-106">Une entrée de fichier journal a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="64f88-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64f88-107">Élément</span><span class="sxs-lookup"><span data-stu-id="64f88-107">Part</span></span></p></th>
<th><p><span data-ttu-id="64f88-108">Description</span><span class="sxs-lookup"><span data-stu-id="64f88-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64f88-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="64f88-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="64f88-110">Chaîne littéral qui indique qu'il s'agit d'une entrée de fichier journal.</span><span class="sxs-lookup"><span data-stu-id="64f88-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64f88-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="64f88-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="64f88-p101">Chemin d'accès complet et nom du fichier. Le nom de fichier habituel est <strong>c:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="64f88-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64f88-114">Le fichier journal contient le nom de l'utilisateur, HRESULT, la date et l'heure de chaque erreur.</span><span class="sxs-lookup"><span data-stu-id="64f88-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

