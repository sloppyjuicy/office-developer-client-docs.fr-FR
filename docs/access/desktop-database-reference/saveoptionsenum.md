---
title: SaveOptionsEnum (référence de base de données de bureau Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314741"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="a984e-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="a984e-102">SaveOptionsEnum</span></span>

<span data-ttu-id="a984e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a984e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a984e-p101">Spécifie si un fichier doit être créé ou remplacé en cas de sauvegarde d'un objet [Stream](stream-object-ado.md). Les valeurs peuvent être combinées avec un opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="a984e-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a984e-106">Constante</span><span class="sxs-lookup"><span data-stu-id="a984e-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="a984e-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="a984e-107">Value</span></span></p></th>
<th><p><span data-ttu-id="a984e-108">Description</span><span class="sxs-lookup"><span data-stu-id="a984e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a984e-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="a984e-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="a984e-110">0,1</span><span class="sxs-lookup"><span data-stu-id="a984e-110">1</span></span></p></td>
<td><p><span data-ttu-id="a984e-p102">Par défaut. Crée un nouveau fichier si le fichier spécifié par le paramètre <em>FileName</em> n'existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="a984e-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a984e-113"><strong>Valeur adSaveCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="a984e-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="a984e-114">n°2</span><span class="sxs-lookup"><span data-stu-id="a984e-114">2</span></span></p></td>
<td><p><span data-ttu-id="a984e-115">Remplace le fichier avec les données de l'objet <strong>Stream</strong> ouvert, si le fichier spécifié par le paramètre <em>Filename</em> existe déjà.</span><span class="sxs-lookup"><span data-stu-id="a984e-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a984e-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a984e-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="a984e-117">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="a984e-117">These constants do not have ADO/WFC equivalents.</span></span>

