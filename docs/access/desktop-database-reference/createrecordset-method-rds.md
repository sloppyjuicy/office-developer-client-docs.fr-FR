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
# <a name="createrecordset-method-rds"></a><span data-ttu-id="a2b42-102">CreateRecordset, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="a2b42-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="a2b42-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2b42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2b42-104">Crée un objet [Recordset](recordset-object-ado.md) vide et déconnecté.</span><span class="sxs-lookup"><span data-stu-id="a2b42-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2b42-105">Syntax</span></span>

<span data-ttu-id="a2b42-106">*.* CreateRecordset(*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="a2b42-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="a2b42-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2b42-107">Parameters</span></span>

|<span data-ttu-id="a2b42-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a2b42-108">Parameter</span></span>|<span data-ttu-id="a2b42-109">Description</span><span class="sxs-lookup"><span data-stu-id="a2b42-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a2b42-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="a2b42-110">*Object*</span></span> |<span data-ttu-id="a2b42-111">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="a2b42-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="a2b42-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="a2b42-112">*ColumnsInfos*</span></span> |<span data-ttu-id="a2b42-113">Tableau de type **Variant** qui contient des attributs et définit chaque colonne de l'objet **Recordset** créé.</span><span class="sxs-lookup"><span data-stu-id="a2b42-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="a2b42-114">Chaque définition de colonne contient un tableau de quatre attributs obligatoires et un attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="a2b42-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="a2b42-115">Le jeu de tableaux de colonnes est ensuite regroupé dans un tableau qui définit l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a2b42-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="a2b42-116">Pour obtenir la liste des attributs, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a2b42-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="a2b42-117">Attributs de tableau de variantes</span><span class="sxs-lookup"><span data-stu-id="a2b42-117">Variant array attributes</span></span>

|<span data-ttu-id="a2b42-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="a2b42-118">Attribute</span></span>|<span data-ttu-id="a2b42-119">Description</span><span class="sxs-lookup"><span data-stu-id="a2b42-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a2b42-120">Nom</span><span class="sxs-lookup"><span data-stu-id="a2b42-120">Name</span></span> |<span data-ttu-id="a2b42-121">Nom de l'en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="a2b42-121">Name of the column header.</span></span>|
|<span data-ttu-id="a2b42-122">Type</span><span class="sxs-lookup"><span data-stu-id="a2b42-122">Type</span></span> |<span data-ttu-id="a2b42-123">Entier du type de données.</span><span class="sxs-lookup"><span data-stu-id="a2b42-123">Integer of the data type.</span></span>|
|<span data-ttu-id="a2b42-124">Size</span><span class="sxs-lookup"><span data-stu-id="a2b42-124">Size</span></span> |<span data-ttu-id="a2b42-125">Entier de la largeur en caractères, quel que soit le type de données.</span><span class="sxs-lookup"><span data-stu-id="a2b42-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="a2b42-126">Nullabilité</span><span class="sxs-lookup"><span data-stu-id="a2b42-126">Nullability</span></span> |<span data-ttu-id="a2b42-127">Valeur de type Boolean.</span><span class="sxs-lookup"><span data-stu-id="a2b42-127">Boolean value.</span></span>|
|<span data-ttu-id="a2b42-128">Échelle (facultatif)</span><span class="sxs-lookup"><span data-stu-id="a2b42-128">Scale (optional)</span></span> |<span data-ttu-id="a2b42-p102">Cet attribut facultatif définit l'échelle des champs numériques. Si cette valeur n'est pas spécifiée, les valeurs numériques sont tronquées à une échelle de trois. La précision n'est pas affectée, mais le nombre de chiffres après la virgule est tronqué après trois.</span><span class="sxs-lookup"><span data-stu-id="a2b42-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a2b42-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2b42-132">Remarks</span></span>

<span data-ttu-id="a2b42-133">L’objet métier côté serveur peut remplir l’objet **Recordset** résultant avec des données provenant d’un fournisseur de données non OLE DB, tel qu’un fichier du système d’exploitation contenant les cours des actions.</span><span class="sxs-lookup"><span data-stu-id="a2b42-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="a2b42-p103">Le tableau suivant répertorie les valeurs de l'énumération [DataTypeEnum](datatypeenum.md) prises en charge par la méthode **CreateRecordset**. Le nombre indiqué correspond au numéro de référence utilisé pour définir des champs.</span><span class="sxs-lookup"><span data-stu-id="a2b42-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="a2b42-p104">Chaque type de données est de longueur fixe ou variable. Les types de longueur fixe doivent être définis par la taille –1, parce que la taille est prédéterminée et que la définition de la taille est toujours obligatoire. Les types de données de longueur variable permettent d'obtenir une taille situé entre 1 et 32767.</span><span class="sxs-lookup"><span data-stu-id="a2b42-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="a2b42-p105">Pour certains types de données variables, il est possible de forcer une conversion du type dans le type indiqué dans la colonne Substitution. Vous ne voyez les substitutions qu'une fois l'objet **Recordset** créé et rempli. Vous pouvez alors vérifier le type de données réel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a2b42-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2b42-142">Longueur</span><span class="sxs-lookup"><span data-stu-id="a2b42-142">Length</span></span></p></th>
<th><p><span data-ttu-id="a2b42-143">Constante</span><span class="sxs-lookup"><span data-stu-id="a2b42-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="a2b42-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2b42-144">Number</span></span></p></th>
<th><p><span data-ttu-id="a2b42-145">Substitution</span><span class="sxs-lookup"><span data-stu-id="a2b42-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-146">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-148">16 </span><span class="sxs-lookup"><span data-stu-id="a2b42-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-149">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-151">2</span><span class="sxs-lookup"><span data-stu-id="a2b42-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-152">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-154">3</span><span class="sxs-lookup"><span data-stu-id="a2b42-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-155">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-157">20</span><span class="sxs-lookup"><span data-stu-id="a2b42-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-158">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-160">17 </span><span class="sxs-lookup"><span data-stu-id="a2b42-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-161">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-163">18 </span><span class="sxs-lookup"><span data-stu-id="a2b42-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-164">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-166">19</span><span class="sxs-lookup"><span data-stu-id="a2b42-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-167">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-169"> 21</span><span class="sxs-lookup"><span data-stu-id="a2b42-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-170">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-172">4 </span><span class="sxs-lookup"><span data-stu-id="a2b42-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-173">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-175">5 </span><span class="sxs-lookup"><span data-stu-id="a2b42-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-176">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-178">6 </span><span class="sxs-lookup"><span data-stu-id="a2b42-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-179">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-181">14 </span><span class="sxs-lookup"><span data-stu-id="a2b42-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-182">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-184">131</span><span class="sxs-lookup"><span data-stu-id="a2b42-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-185">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-187">11</span><span class="sxs-lookup"><span data-stu-id="a2b42-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-188">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-190">10</span><span class="sxs-lookup"><span data-stu-id="a2b42-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-191">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-193">72</span><span class="sxs-lookup"><span data-stu-id="a2b42-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-194">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-196">7 </span><span class="sxs-lookup"><span data-stu-id="a2b42-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-197">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-199">133</span><span class="sxs-lookup"><span data-stu-id="a2b42-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-200">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-202">134</span><span class="sxs-lookup"><span data-stu-id="a2b42-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-203">Fixed</span><span class="sxs-lookup"><span data-stu-id="a2b42-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="a2b42-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-205">135</span><span class="sxs-lookup"><span data-stu-id="a2b42-205">135</span></span></p></td>
<td><p><span data-ttu-id="a2b42-206">7 </span><span class="sxs-lookup"><span data-stu-id="a2b42-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-207">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-209">8 </span><span class="sxs-lookup"><span data-stu-id="a2b42-209">8</span></span></p></td>
<td><p><span data-ttu-id="a2b42-210">130</span><span class="sxs-lookup"><span data-stu-id="a2b42-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-211">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-213">129</span><span class="sxs-lookup"><span data-stu-id="a2b42-213">129</span></span></p></td>
<td><p><span data-ttu-id="a2b42-214">200</span><span class="sxs-lookup"><span data-stu-id="a2b42-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-215">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-217">200</span><span class="sxs-lookup"><span data-stu-id="a2b42-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-218">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-220">201</span><span class="sxs-lookup"><span data-stu-id="a2b42-220">201</span></span></p></td>
<td><p><span data-ttu-id="a2b42-221">200</span><span class="sxs-lookup"><span data-stu-id="a2b42-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-222">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-224">130</span><span class="sxs-lookup"><span data-stu-id="a2b42-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-225">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-227">202</span><span class="sxs-lookup"><span data-stu-id="a2b42-227">202</span></span></p></td>
<td><p><span data-ttu-id="a2b42-228">130</span><span class="sxs-lookup"><span data-stu-id="a2b42-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-229">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-231">203</span><span class="sxs-lookup"><span data-stu-id="a2b42-231">203</span></span></p></td>
<td><p><span data-ttu-id="a2b42-232">130</span><span class="sxs-lookup"><span data-stu-id="a2b42-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-233">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-235">128</span><span class="sxs-lookup"><span data-stu-id="a2b42-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b42-236">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-238">204</span><span class="sxs-lookup"><span data-stu-id="a2b42-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b42-239">Variable</span><span class="sxs-lookup"><span data-stu-id="a2b42-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="a2b42-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a2b42-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b42-241">205</span><span class="sxs-lookup"><span data-stu-id="a2b42-241">205</span></span></p></td>
<td><p><span data-ttu-id="a2b42-242">204</span><span class="sxs-lookup"><span data-stu-id="a2b42-242">204</span></span></p></td>
</tr>
</tbody>
</table>

