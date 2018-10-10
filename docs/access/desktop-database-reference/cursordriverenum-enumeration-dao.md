---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcce8eefad7fcad7dee7e46274ffc45125dc36c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471444"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="05bc5-102">CursorDriverEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="05bc5-102">CursorDriverEnum Enumeration (DAO)</span></span>


<span data-ttu-id="05bc5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05bc5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05bc5-104">Spécifie le type de pilote de curseur.</span><span class="sxs-lookup"><span data-stu-id="05bc5-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05bc5-105">Nom</span><span class="sxs-lookup"><span data-stu-id="05bc5-105">Name</span></span></p></th>
<th><p><span data-ttu-id="05bc5-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="05bc5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="05bc5-107">Description</span><span class="sxs-lookup"><span data-stu-id="05bc5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05bc5-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="05bc5-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="05bc5-109">3</span><span class="sxs-lookup"><span data-stu-id="05bc5-109">3</span></span></p></td>
<td><p><span data-ttu-id="05bc5-p101">Utilise toujours la bibliothèque de curseurs FoxPro. Cette option est obligatoire pour effectuer des mises à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="05bc5-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05bc5-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="05bc5-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="05bc5-113">-1</span><span class="sxs-lookup"><span data-stu-id="05bc5-113">-1</span></span></p></td>
<td><p><span data-ttu-id="05bc5-114">(Valeur par défaut) Utilise des curseurs du côté serveur si le serveur les prend en charge. Si ce n'est pas le cas, utilise la bibliothèque de curseurs ODBC.</span><span class="sxs-lookup"><span data-stu-id="05bc5-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05bc5-115">en d’autres termes</span><span class="sxs-lookup"><span data-stu-id="05bc5-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="05bc5-116">4</span><span class="sxs-lookup"><span data-stu-id="05bc5-116">4</span></span></p></td>
<td><p><span data-ttu-id="05bc5-117">Ouvre tous les curseurs (c'est-à-dire, les objets <strong>Recordset</strong> ) en tant que type avant uniquement, en lecture seule, avec une taille de jeu de lignes de 1.</span><span class="sxs-lookup"><span data-stu-id="05bc5-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="05bc5-118">Également appelé &quot;requêtes sans curseur.&quot;</span><span class="sxs-lookup"><span data-stu-id="05bc5-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05bc5-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="05bc5-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="05bc5-120">1</span><span class="sxs-lookup"><span data-stu-id="05bc5-120">1</span></span></p></td>
<td><p><span data-ttu-id="05bc5-p103">Utilise toujours la bibliothèque de curseurs ODBC. Cette option permet d'améliorer les performances pour les jeux de résultats de petite taille. Les performances diminuent toutefois rapidement pour les jeux de résultats volumineux.</span><span class="sxs-lookup"><span data-stu-id="05bc5-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05bc5-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="05bc5-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="05bc5-124">2</span><span class="sxs-lookup"><span data-stu-id="05bc5-124">2</span></span></p></td>
<td><p><span data-ttu-id="05bc5-p104">Utilise toujours des curseurs du côté serveur. Cette option améliore les performances pour la plupart des opérations importantes. Elle risque toutefois d'augmenter le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="05bc5-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

