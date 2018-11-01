---
title: Types de données SQL (référence de base de données du bureau Access)
TOCTitle: SQL Data Types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fd49861af896ae1c2d55a80665f119662c0baf53
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880396"
---
# <a name="sql-data-types"></a><span data-ttu-id="9e70f-102">Types de données SQL</span><span class="sxs-lookup"><span data-stu-id="9e70f-102">SQL Data Types</span></span>


<span data-ttu-id="9e70f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e70f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e70f-104">Les types de données SQL du moteur de base de données Microsoft Access comprennent 13 types de données principaux définis par le moteur de base de données Microsoft® Jet et plusieurs synonymes valides reconnus pour ces types de données.</span><span class="sxs-lookup"><span data-stu-id="9e70f-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft® Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="9e70f-p101">Le tableau suivant répertorie les principaux types de données. Les synonymes sont indiqués dans [Mots réservés SQL du moteur de base de données Microsoft Access](sql-reserved-words.md).</span><span class="sxs-lookup"><span data-stu-id="9e70f-p101">The following table lists the primary data types. The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e70f-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="9e70f-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="9e70f-108">Taille</span><span class="sxs-lookup"><span data-stu-id="9e70f-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="9e70f-109">Description</span><span class="sxs-lookup"><span data-stu-id="9e70f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="9e70f-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="9e70f-111">1 octet par caractère</span><span class="sxs-lookup"><span data-stu-id="9e70f-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="9e70f-p102">N'importe quel type de données peut être stocké dans un champ de ce type. Aucune conversion des données (par exemple, en texte) n'est effectuée. La manière dont les données sont entrées dans un champ binaire détermine comment elles apparaîtront une fois produites.</span><span class="sxs-lookup"><span data-stu-id="9e70f-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-115">BIT</span><span class="sxs-lookup"><span data-stu-id="9e70f-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="9e70f-116">1 octet</span><span class="sxs-lookup"><span data-stu-id="9e70f-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="9e70f-117">Les valeurs Oui et Non et les champs qui contiennent une de ces deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="9e70f-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="9e70f-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="9e70f-119">1 octet</span><span class="sxs-lookup"><span data-stu-id="9e70f-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="9e70f-120">Une valeur entière entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="9e70f-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="9e70f-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="9e70f-122">8 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-123">Un entier décalé entre – 922 337 203 685 477,5808 et 922 337 203 685 477,5807.</span><span class="sxs-lookup"><span data-stu-id="9e70f-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-124">DATETIME (voir DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="9e70f-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="9e70f-125">8 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-126">Valeur de date ou d'heure entre les années 100 et 9999.</span><span class="sxs-lookup"><span data-stu-id="9e70f-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="9e70f-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="9e70f-128">128 bits</span><span class="sxs-lookup"><span data-stu-id="9e70f-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="9e70f-129">Numéro d'identification unique utilisé avec des appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9e70f-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-130">REAL</span><span class="sxs-lookup"><span data-stu-id="9e70f-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="9e70f-131">4 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-132">Valeur à virgule flottante (simple précision) comprise entre – 3,402823E38 et – 1,401298E-45 pour les valeurs négatives et entre 1,401298E-45 et 3,402823E38 pour les valeurs positives et 0.</span><span class="sxs-lookup"><span data-stu-id="9e70f-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9e70f-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="9e70f-134">8 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-135">Valeur à virgule flottante (double précision) comprise entre – 1,79769313486232E308 et – 4,94065645841247E-324 pour les valeurs négatives et entre 4,94065645841247E-324 et 1,79769313486232E308 pour les valeurs positives et 0.</span><span class="sxs-lookup"><span data-stu-id="9e70f-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="9e70f-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="9e70f-137">2 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-p103">Entier court entre – 32 768 et 32 767. (Voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9e70f-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9e70f-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="9e70f-141">4 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-p104">Entier long entre – 2 147 483 648 et 2 147 483 647. (Voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9e70f-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="9e70f-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="9e70f-145">17 octets</span><span class="sxs-lookup"><span data-stu-id="9e70f-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="9e70f-p105">Type de données numériques exactes qui contient des valeurs entre 1028 - 1 et - 1028 - 1. Vous pouvez définir la précision (1 - 28) et l'échelle (0 - précision définie). La précision et l'échelle par défaut sont respectivement 18 et 0.</span><span class="sxs-lookup"><span data-stu-id="9e70f-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="9e70f-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="9e70f-150">2 octets par caractère (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9e70f-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9e70f-151">Entre 0 et 2,14 gigaoctets maximum.</span><span class="sxs-lookup"><span data-stu-id="9e70f-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e70f-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="9e70f-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="9e70f-153">En fonction des besoins</span><span class="sxs-lookup"><span data-stu-id="9e70f-153">As required</span></span></p></td>
<td><p><span data-ttu-id="9e70f-p106">Entre 0 et 2,14 gigaoctets maximum. Utilisé pour les objets OLE.</span><span class="sxs-lookup"><span data-stu-id="9e70f-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e70f-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="9e70f-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="9e70f-157">2 octets par caractère (voir Remarques)</span><span class="sxs-lookup"><span data-stu-id="9e70f-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="9e70f-158">Entre zéro et 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="9e70f-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="9e70f-p107">La valeur de départ et la valeur incrémentielle peuvent être modifiées à l'aide d'une <A href="alter-table-statement-microsoft-access-sql.md">instruction ALTER TABLE</A>. Les nouvelles lignes insérées dans la table comportent des valeurs basées sur la nouvelle valeur de départ et la nouvelle valeur incrémentielle qui sont automatiquement générées pour la colonne. Si ces nouvelles valeurs peuvent produire des valeurs qui correspondent à celles générées à partir de la valeur de départ et de la valeur incrémentielle d'origine, des valeurs en double sont générées. Si la colonne est une clé primaire, l'insertion de nouvelles lignes peut produire des erreurs lorsque des valeurs en double sont générées.</span><span class="sxs-lookup"><span data-stu-id="9e70f-p107">Both the seed and the increment can be modified using an <A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE statement</A>. New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span></P>
> <LI>
> <P><span data-ttu-id="9e70f-p108">Pour rechercher la dernière valeur qui a été utilisée pour une colonne incrémentée automatiquement, vous pouvez utiliser l'instruction suivante : SELECT @@IDENTITY. En revanche, vous ne pouvez pas spécifier le nom d'une table. La valeur renvoyée provient de la dernière table contenant une colonne incrémentée automatiquement qui a été dupliquée.</span><span class="sxs-lookup"><span data-stu-id="9e70f-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span></P></LI></UL>


