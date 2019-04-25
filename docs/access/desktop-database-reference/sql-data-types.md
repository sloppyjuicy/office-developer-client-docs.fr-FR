---
title: Types de données SQL (référence de base de données de bureau Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308580"
---
# <a name="sql-data-types"></a><span data-ttu-id="a8d33-102">Types de données SQL</span><span class="sxs-lookup"><span data-stu-id="a8d33-102">SQL data types</span></span>

<span data-ttu-id="a8d33-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8d33-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8d33-104">Les types de données SQL du moteur de base de données Microsoft Access comprennent 13 types de données principaux définis par le moteur de base de données Microsoft Jet et plusieurs synonymes valides reconnus pour ces types de données.</span><span class="sxs-lookup"><span data-stu-id="a8d33-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft® Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="a8d33-105">Le tableau suivant répertorie les types de données principaux.</span><span class="sxs-lookup"><span data-stu-id="a8d33-105">The following table lists the primary data types.</span></span> <span data-ttu-id="a8d33-106">Les synonymes sont identifiés dans [mots réservés SQL du moteur de base de données Microsoft Access](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="a8d33-106">The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8d33-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a8d33-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="a8d33-108">Taille</span><span class="sxs-lookup"><span data-stu-id="a8d33-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="a8d33-109">Description</span><span class="sxs-lookup"><span data-stu-id="a8d33-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="a8d33-110">Binary</span></span></p></td>
<td><p><span data-ttu-id="a8d33-111">1 octet par caractère</span><span class="sxs-lookup"><span data-stu-id="a8d33-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="a8d33-p102">Tout type de données peut être stocké dans un champ de ce type. Aucune traduction des données (par exemple, en texte) n’est effectuée. La manière dont les données sont entrées dans un champ binaire détermine la façon dont elles s’affichent en tant que sortie.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-115">BIT</span><span class="sxs-lookup"><span data-stu-id="a8d33-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="a8d33-116">1 octet</span><span class="sxs-lookup"><span data-stu-id="a8d33-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="a8d33-117">Valeurs Oui et Non, et champs contenant uniquement l’une des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="a8d33-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="a8d33-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="a8d33-119">1 octet</span><span class="sxs-lookup"><span data-stu-id="a8d33-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="a8d33-120">Valeur entière comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a8d33-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="a8d33-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="a8d33-122">8 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-123">Entier mis à l’échelle dont la valeur est comprise entre-922 337 203 685 477,5808 et 922 337 203 685 477,5807.</span><span class="sxs-lookup"><span data-stu-id="a8d33-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-124">DATETIME (voir DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="a8d33-124">DATETIME
(See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="a8d33-125">8 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-126">Valeur de date ou d’heure comprise entre les années 100 et 9999.</span><span class="sxs-lookup"><span data-stu-id="a8d33-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="a8d33-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="a8d33-128">128 bits</span><span class="sxs-lookup"><span data-stu-id="a8d33-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="a8d33-129">Numéro d’identification unique utilisé avec des appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a8d33-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-130">REAL</span><span class="sxs-lookup"><span data-stu-id="a8d33-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="a8d33-131">4 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-132">Valeur à virgule flottante simple précision avec une plage de -3,402823E38 à -1,401298E-45 pour les valeurs négatives, de 1,401298E-45 à 3,402823E38 pour les valeurs positives, et 0.</span><span class="sxs-lookup"><span data-stu-id="a8d33-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a8d33-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="a8d33-134">8 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-135">Une valeur à virgule flottante double précision avec une plage de -1,79769313486232E308 à -4,94065645841247E-324 pour les valeurs négatives, de 4,94065645841247E-324 à 1,79769313486232E308 pour les valeurs positives, et 0.</span><span class="sxs-lookup"><span data-stu-id="a8d33-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="a8d33-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="a8d33-137">2 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-p103">Entier court compris entre -32 768 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="a8d33-140">Integer</span></span></p></td>
<td><p><span data-ttu-id="a8d33-141">4 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-p104">Entier long compris entre -2 147 483 648 et 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="a8d33-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="a8d33-145">17 octets</span><span class="sxs-lookup"><span data-stu-id="a8d33-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="a8d33-p105">Type de données numériques exactes qui contient des valeurs comprises entre 1 028-1 et -1 028-1. Vous pouvez définir la précision (1-28) et l’échelle (0-précision définie). La précision et l’échelle par défaut sont respectivement de 18 et 0.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="a8d33-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="a8d33-150">2 octets par caractère (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="a8d33-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a8d33-151">Zéro à un maximum de 2,14 Go.</span><span class="sxs-lookup"><span data-stu-id="a8d33-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d33-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="a8d33-152">Image</span></span></p></td>
<td><p><span data-ttu-id="a8d33-153">Si nécessaire</span><span class="sxs-lookup"><span data-stu-id="a8d33-153">As required</span></span></p></td>
<td><p><span data-ttu-id="a8d33-p106">Zéro à un maximum de 2,14 Go. Utilisé pour les objets OLE.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d33-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="a8d33-156">Character</span></span></p></td>
<td><p><span data-ttu-id="a8d33-157">2 octets par caractère (voir Remarque)</span><span class="sxs-lookup"><span data-stu-id="a8d33-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="a8d33-158">Jusqu’à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="a8d33-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - <span data-ttu-id="a8d33-p107">La valeur de départ et l’incrément peuvent être modifiés à l’aide un [instruction TABLE modifier](alter-table-statement-microsoft-access-sql.md). Nouvelles lignes insérées dans la table comportent des valeurs basées sur la nouvelle valeur de départ et les valeurs incrément, qui sont générées automatiquement pour la colonne. Si la nouvelle valeur de départ et l’incrément pouvant rendement valeurs qui correspondent aux valeurs générées basé sur la valeur de départ et l’incrément précédente, les doublons seront générées. Si la colonne est une clé primaire, puis en insérant nouvelles lignes peut entraîner des erreurs lorsque les valeurs en double sont générés.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p107">Both the seed and the increment can be modified using an [ALTER TABLE statement](alter-table-statement-microsoft-access-sql.md). New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span>
> - <span data-ttu-id="a8d33-p108">Pour rechercher la dernière valeur que vous avez utilisée pour une colonne incrément automatique, vous pouvez utiliser l’instruction suivante : sélectionnez @@IDENTITY. Vous ne pouvez pas spécifier un nom de tableau. La valeur renvoyée est à partir de la dernière table contenant une colonne incrément automatique qui a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a8d33-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span>
