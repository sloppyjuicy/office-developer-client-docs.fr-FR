---
title: CreateRecordset, méthode (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295337"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="e7a1c-102">CreateRecordset, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="e7a1c-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="e7a1c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7a1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7a1c-104">Crée un objet [Recordset](recordset-object-ado.md) vide et déconnecté.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a1c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7a1c-105">Syntax</span></span>

<span data-ttu-id="e7a1c-106">*objet*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="e7a1c-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e7a1c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7a1c-107">Parameters</span></span>

|<span data-ttu-id="e7a1c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a1c-108">Parameter</span></span>|<span data-ttu-id="e7a1c-109">Description</span><span class="sxs-lookup"><span data-stu-id="e7a1c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e7a1c-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="e7a1c-110">*Object*</span></span> |<span data-ttu-id="e7a1c-111">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e7a1c-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="e7a1c-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="e7a1c-112">*ColumnsInfos*</span></span> |<span data-ttu-id="e7a1c-113">Tableau de type **Variant** qui contient des attributs et définit chaque colonne de l'objet **Recordset** créé.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="e7a1c-114">Chaque définition de colonne contient un tableau de quatre attributs obligatoires et un attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="e7a1c-115">Le jeu de tableaux de colonnes est ensuite regroupé dans un tableau qui définit l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="e7a1c-116">Pour obtenir la liste des attributs, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="e7a1c-117">Attributs de tableau de variantes</span><span class="sxs-lookup"><span data-stu-id="e7a1c-117">Variant array attributes</span></span>

|<span data-ttu-id="e7a1c-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="e7a1c-118">Attribute</span></span>|<span data-ttu-id="e7a1c-119">Description</span><span class="sxs-lookup"><span data-stu-id="e7a1c-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e7a1c-120">Nom</span><span class="sxs-lookup"><span data-stu-id="e7a1c-120">Name</span></span> |<span data-ttu-id="e7a1c-121">Nom de l'en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-121">Name of the column header.</span></span>|
|<span data-ttu-id="e7a1c-122">Type</span><span class="sxs-lookup"><span data-stu-id="e7a1c-122">Type</span></span> |<span data-ttu-id="e7a1c-123">Entier du type de données.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-123">Integer of the data type.</span></span>|
|<span data-ttu-id="e7a1c-124">Taille</span><span class="sxs-lookup"><span data-stu-id="e7a1c-124">Size</span></span> |<span data-ttu-id="e7a1c-125">Entier de la largeur en caractères, quel que soit le type de données.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="e7a1c-126">Possibilité de valeur null</span><span class="sxs-lookup"><span data-stu-id="e7a1c-126">Nullability</span></span> |<span data-ttu-id="e7a1c-127">Valeur de type Boolean.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-127">Boolean value.</span></span>|
|<span data-ttu-id="e7a1c-128">Homothétie (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e7a1c-128">Scale (optional)</span></span> |<span data-ttu-id="e7a1c-p102">Cet attribut facultatif définit l'échelle des champs numériques. Si cette valeur n'est pas spécifiée, les valeurs numériques sont tronquées à une échelle de trois. La précision n'est pas affectée, mais le nombre de chiffres après la virgule est tronqué après trois.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e7a1c-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7a1c-132">Remarks</span></span>

<span data-ttu-id="e7a1c-133">L’objet métier côté serveur peut remplir l’objet **Recordset** résultant avec des données provenant d’un fournisseur de données non OLE DB, tel qu’un fichier du système d’exploitation contenant les cours des actions.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="e7a1c-p103">Le tableau suivant répertorie les valeurs de l'énumération [DataTypeEnum](datatypeenum.md) prises en charge par la méthode **CreateRecordset**. Le nombre indiqué correspond au numéro de référence utilisé pour définir des champs.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="e7a1c-p104">Chaque type de données est de longueur fixe ou variable. Les types de longueur fixe doivent être définis par la taille –1, parce que la taille est prédéterminée et que la définition de la taille est toujours obligatoire. Les types de données de longueur variable permettent d'obtenir une taille situé entre 1 et 32767.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="e7a1c-p105">Pour certains types de données variables, il est possible de forcer une conversion du type dans le type indiqué dans la colonne Substitution. Vous ne voyez les substitutions qu'une fois l'objet **Recordset** créé et rempli. Vous pouvez alors vérifier le type de données réel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e7a1c-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7a1c-142">Longueur</span><span class="sxs-lookup"><span data-stu-id="e7a1c-142">Length</span></span></p></th>
<th><p><span data-ttu-id="e7a1c-143">Constante</span><span class="sxs-lookup"><span data-stu-id="e7a1c-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="e7a1c-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="e7a1c-144">Number</span></span></p></th>
<th><p><span data-ttu-id="e7a1c-145">Substitution</span><span class="sxs-lookup"><span data-stu-id="e7a1c-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-146">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-148">Seiz</span><span class="sxs-lookup"><span data-stu-id="e7a1c-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-149">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-151">n°2</span><span class="sxs-lookup"><span data-stu-id="e7a1c-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-152">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-154">3</span><span class="sxs-lookup"><span data-stu-id="e7a1c-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-155">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-157">vingtaine</span><span class="sxs-lookup"><span data-stu-id="e7a1c-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-158">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-160">cm</span><span class="sxs-lookup"><span data-stu-id="e7a1c-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-161">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-163">18</span><span class="sxs-lookup"><span data-stu-id="e7a1c-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-164">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-166">neuf</span><span class="sxs-lookup"><span data-stu-id="e7a1c-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-167">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-169">21</span><span class="sxs-lookup"><span data-stu-id="e7a1c-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-170">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-172">4</span><span class="sxs-lookup"><span data-stu-id="e7a1c-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-173">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-175">disque</span><span class="sxs-lookup"><span data-stu-id="e7a1c-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-176">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-178">6.x</span><span class="sxs-lookup"><span data-stu-id="e7a1c-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-179">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-181">13</span><span class="sxs-lookup"><span data-stu-id="e7a1c-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-182">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-184">131</span><span class="sxs-lookup"><span data-stu-id="e7a1c-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-185">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-187">a4</span><span class="sxs-lookup"><span data-stu-id="e7a1c-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-188">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-190">10</span><span class="sxs-lookup"><span data-stu-id="e7a1c-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-191">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-193">72</span><span class="sxs-lookup"><span data-stu-id="e7a1c-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-194">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-196">7j/7</span><span class="sxs-lookup"><span data-stu-id="e7a1c-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-197">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-199">133</span><span class="sxs-lookup"><span data-stu-id="e7a1c-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-200">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-202">134</span><span class="sxs-lookup"><span data-stu-id="e7a1c-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-203">Fixed</span><span class="sxs-lookup"><span data-stu-id="e7a1c-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-205">135</span><span class="sxs-lookup"><span data-stu-id="e7a1c-205">135</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-206">7j/7</span><span class="sxs-lookup"><span data-stu-id="e7a1c-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-207">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-209">8bits</span><span class="sxs-lookup"><span data-stu-id="e7a1c-209">8</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-210">130</span><span class="sxs-lookup"><span data-stu-id="e7a1c-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-211">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-213">129</span><span class="sxs-lookup"><span data-stu-id="e7a1c-213">129</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-214">200</span><span class="sxs-lookup"><span data-stu-id="e7a1c-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-215">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-217">200</span><span class="sxs-lookup"><span data-stu-id="e7a1c-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-218">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-220">201</span><span class="sxs-lookup"><span data-stu-id="e7a1c-220">201</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-221">200</span><span class="sxs-lookup"><span data-stu-id="e7a1c-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-222">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-224">130</span><span class="sxs-lookup"><span data-stu-id="e7a1c-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-225">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-227">202</span><span class="sxs-lookup"><span data-stu-id="e7a1c-227">202</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-228">130</span><span class="sxs-lookup"><span data-stu-id="e7a1c-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-229">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-231">203</span><span class="sxs-lookup"><span data-stu-id="e7a1c-231">203</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-232">130</span><span class="sxs-lookup"><span data-stu-id="e7a1c-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-233">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-235">128</span><span class="sxs-lookup"><span data-stu-id="e7a1c-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7a1c-236">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-238">204</span><span class="sxs-lookup"><span data-stu-id="e7a1c-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7a1c-239">Variable</span><span class="sxs-lookup"><span data-stu-id="e7a1c-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e7a1c-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e7a1c-241">205</span><span class="sxs-lookup"><span data-stu-id="e7a1c-241">205</span></span></p></td>
<td><p><span data-ttu-id="e7a1c-242">204</span><span class="sxs-lookup"><span data-stu-id="e7a1c-242">204</span></span></p></td>
</tr>
</tbody>
</table>

