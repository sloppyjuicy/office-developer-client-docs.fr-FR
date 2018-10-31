---
title: SaveOptionsEnum (référence de base de données du bureau Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ffd37090b264e434b5fd3750f474122f8da4bfbb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861903"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="16723-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="16723-102">SaveOptionsEnum</span></span>

<span data-ttu-id="16723-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="16723-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="16723-p101">Spécifie si un fichier doit être créé ou remplacé en cas de sauvegarde d'un objet [Stream](stream-object-ado.md). Les valeurs peuvent être combinées avec un opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="16723-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16723-106">Constant</span><span class="sxs-lookup"><span data-stu-id="16723-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="16723-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="16723-107">Value</span></span></p></th>
<th><p><span data-ttu-id="16723-108">Description</span><span class="sxs-lookup"><span data-stu-id="16723-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16723-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="16723-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="16723-110">1</span><span class="sxs-lookup"><span data-stu-id="16723-110">1</span></span></p></td>
<td><p><span data-ttu-id="16723-p102">Par défaut. Crée un nouveau fichier si le fichier spécifié par le paramètre <em>FileName</em> n'existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="16723-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16723-113"><strong>valeur adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="16723-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="16723-114">2</span><span class="sxs-lookup"><span data-stu-id="16723-114">2</span></span></p></td>
<td><p><span data-ttu-id="16723-115">Remplace le fichier avec les données de l'objet <strong>Stream</strong> ouvert, si le fichier spécifié par le paramètre <em>Filename</em> existe déjà.</span><span class="sxs-lookup"><span data-stu-id="16723-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="16723-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="16723-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="16723-117">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="16723-117">These constants do not have ADO/WFC equivalents.</span></span>

