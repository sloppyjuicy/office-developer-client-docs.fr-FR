---
title: AllowNullsEnum (référence de base de données du bureau Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04e67584e0f0c2eeb5a12e34fdf98a84cc1da852
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470762"
---
# <a name="allownullsenum"></a><span data-ttu-id="b9cd2-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="b9cd2-102">AllowNullsEnum</span></span>


<span data-ttu-id="b9cd2-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9cd2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b9cd2-104">Indique si des enregistrements contenant des valeurs Null sont indexés.</span><span class="sxs-lookup"><span data-stu-id="b9cd2-104">Specifies whether records with null values are indexed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9cd2-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b9cd2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b9cd2-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9cd2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b9cd2-107">Description</span><span class="sxs-lookup"><span data-stu-id="b9cd2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9cd2-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="b9cd2-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="b9cd2-109">0</span><span class="sxs-lookup"><span data-stu-id="b9cd2-109">0</span></span></p></td>
<td><p><span data-ttu-id="b9cd2-p101">L'index autorise les entrées dans lesquelles les colonnes clés sont Null. L'entrée est insérée dans l'index lorsqu'une valeur Null est entrée dans une colonne clé.</span><span class="sxs-lookup"><span data-stu-id="b9cd2-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9cd2-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="b9cd2-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="b9cd2-113">1</span><span class="sxs-lookup"><span data-stu-id="b9cd2-113">1</span></span></p></td>
<td><p><span data-ttu-id="b9cd2-p102">Valeur par défaut. L'index n'autorise pas d'entrées dans lesquelles les colonnes clés ont la valeur Null. Une erreur se produit lorsqu'une valeur Null est entrée dans une colonne clé.</span><span class="sxs-lookup"><span data-stu-id="b9cd2-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9cd2-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="b9cd2-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="b9cd2-118">2</span><span class="sxs-lookup"><span data-stu-id="b9cd2-118">2</span></span></p></td>
<td><p><span data-ttu-id="b9cd2-p103">L'index n'insère pas d'entrée contenant des clés de valeur Null. Si une valeur Null est entrée dans une colonne clé, l'entrée est ignorée et aucune erreur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="b9cd2-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9cd2-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="b9cd2-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="b9cd2-122">4</span><span class="sxs-lookup"><span data-stu-id="b9cd2-122">4</span></span></p></td>
<td><p><span data-ttu-id="b9cd2-p104">L'index n'insère pas d'entrée où une colonne clé contient une valeur Null. Dans le cas d'un index possédant une clé multicolonne, si une valeur Null est entrée dans une colonne, l'entrée est ignorée et aucune erreur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="b9cd2-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

