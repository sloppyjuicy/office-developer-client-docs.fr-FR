---
title: CreateRecordset, méthode (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 696daaeb060387d5f3ca454ef665517a8ff7be74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469336"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="6dc3b-102">CreateRecordset, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="6dc3b-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="6dc3b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dc3b-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6dc3b-104">Crée un objet [Recordset](recordset-object-ado.md) vide et déconnecté.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-105">Syntax</span></span>

<span data-ttu-id="6dc3b-106">*objet*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="6dc3b-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6dc3b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6dc3b-107">Parameters</span></span>

  - <span data-ttu-id="6dc3b-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="6dc3b-108">*Object*</span></span>

  - <span data-ttu-id="6dc3b-109">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="6dc3b-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="6dc3b-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="6dc3b-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="6dc3b-p101">Tableau de type **Variant** qui contient des attributs et définit chaque colonne de l'objet **Recordset** créé. Chaque définition de colonne contient un tableau de quatre attributs obligatoires et un attribut facultatif. Le jeu de tableaux de colonnes est ensuite regroupé dans un tableau qui définit l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="6dc3b-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="6dc3b-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="6dc3b-115">Description</span><span class="sxs-lookup"><span data-stu-id="6dc3b-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="6dc3b-116">Name</span><span class="sxs-lookup"><span data-stu-id="6dc3b-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="6dc3b-117">Nom de l'en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="6dc3b-118">Type</span><span class="sxs-lookup"><span data-stu-id="6dc3b-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="6dc3b-119">Entier du type de données.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="6dc3b-120">Size</span><span class="sxs-lookup"><span data-stu-id="6dc3b-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="6dc3b-121">Entier de la largeur en caractères, quel que soit le type de données.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="6dc3b-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="6dc3b-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="6dc3b-123">Valeur de type Boolean.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="6dc3b-124">Scale (Échelle)</span><span class="sxs-lookup"><span data-stu-id="6dc3b-124">Scale</span></span><br />
<span data-ttu-id="6dc3b-125">(Facultatif)</span><span class="sxs-lookup"><span data-stu-id="6dc3b-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="6dc3b-p102">Cet attribut facultatif définit l'échelle des champs numériques. Si cette valeur n'est pas spécifiée, les valeurs numériques sont tronquées à une échelle de trois. La précision n'est pas affectée, mais le nombre de chiffres après la virgule est tronqué après trois.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="6dc3b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="6dc3b-129">Remarks</span></span>

<span data-ttu-id="6dc3b-130">L'objet métier côté serveur peut remplir l'objet **Recordset** résultant avec des données provenant d'un fournisseur de données non OLE DB, tel qu'un fichier du système d'exploitation contenant les cours des actions.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="6dc3b-p103">Le tableau suivant répertorie les valeurs de l'énumération [DataTypeEnum](datatypeenum.md) prises en charge par la méthode **CreateRecordset**. Le nombre indiqué correspond au numéro de référence utilisé pour définir des champs.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="6dc3b-p104">Chaque type de données est de longueur fixe ou variable. Les types de longueur fixe doivent être définis par la taille –1, parce que la taille est prédéterminée et que la définition de la taille est toujours obligatoire. Les types de données de longueur variable permettent d'obtenir une taille situé entre 1 et 32767.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="6dc3b-p105">Pour certains types de données variables, il est possible de forcer une conversion du type dans le type indiqué dans la colonne Substitution. Vous ne voyez les substitutions qu'une fois l'objet **Recordset** créé et rempli. Vous pouvez alors vérifier le type de données réel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="6dc3b-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6dc3b-139">Longueur</span><span class="sxs-lookup"><span data-stu-id="6dc3b-139">Length</span></span></p></th>
<th><p><span data-ttu-id="6dc3b-140">Constante</span><span class="sxs-lookup"><span data-stu-id="6dc3b-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="6dc3b-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="6dc3b-141">Number</span></span></p></th>
<th><p><span data-ttu-id="6dc3b-142">Substitution</span><span class="sxs-lookup"><span data-stu-id="6dc3b-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-143">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-145">16</span><span class="sxs-lookup"><span data-stu-id="6dc3b-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-146">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-148">2</span><span class="sxs-lookup"><span data-stu-id="6dc3b-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-149">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-150"><strong>tous les types</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-151">3</span><span class="sxs-lookup"><span data-stu-id="6dc3b-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-152">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-154">20</span><span class="sxs-lookup"><span data-stu-id="6dc3b-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-155">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-157">17</span><span class="sxs-lookup"><span data-stu-id="6dc3b-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-158">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-160">18</span><span class="sxs-lookup"><span data-stu-id="6dc3b-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-161">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-163">19</span><span class="sxs-lookup"><span data-stu-id="6dc3b-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-164">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-166">21</span><span class="sxs-lookup"><span data-stu-id="6dc3b-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-167">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-169">4</span><span class="sxs-lookup"><span data-stu-id="6dc3b-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-170">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-171"><strong>longueur fixe</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-172">5</span><span class="sxs-lookup"><span data-stu-id="6dc3b-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-173">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-175">6</span><span class="sxs-lookup"><span data-stu-id="6dc3b-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-176">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-178">14</span><span class="sxs-lookup"><span data-stu-id="6dc3b-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-179">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-181">131</span><span class="sxs-lookup"><span data-stu-id="6dc3b-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-182">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-184">11</span><span class="sxs-lookup"><span data-stu-id="6dc3b-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-185">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-187">10</span><span class="sxs-lookup"><span data-stu-id="6dc3b-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-188">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-190">72</span><span class="sxs-lookup"><span data-stu-id="6dc3b-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-191">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-193">7</span><span class="sxs-lookup"><span data-stu-id="6dc3b-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-194">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-196">133</span><span class="sxs-lookup"><span data-stu-id="6dc3b-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-197">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-199">134</span><span class="sxs-lookup"><span data-stu-id="6dc3b-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-200">Fixe</span><span class="sxs-lookup"><span data-stu-id="6dc3b-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-202">135</span><span class="sxs-lookup"><span data-stu-id="6dc3b-202">135</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-203">7</span><span class="sxs-lookup"><span data-stu-id="6dc3b-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-204">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-206">8</span><span class="sxs-lookup"><span data-stu-id="6dc3b-206">8</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-207">130</span><span class="sxs-lookup"><span data-stu-id="6dc3b-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-208">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-210">129</span><span class="sxs-lookup"><span data-stu-id="6dc3b-210">129</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-211">200</span><span class="sxs-lookup"><span data-stu-id="6dc3b-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-212">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-214">200</span><span class="sxs-lookup"><span data-stu-id="6dc3b-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-215">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-217">201</span><span class="sxs-lookup"><span data-stu-id="6dc3b-217">201</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-218">200</span><span class="sxs-lookup"><span data-stu-id="6dc3b-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-219">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-221">130</span><span class="sxs-lookup"><span data-stu-id="6dc3b-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-222">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-224">202</span><span class="sxs-lookup"><span data-stu-id="6dc3b-224">202</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-225">130</span><span class="sxs-lookup"><span data-stu-id="6dc3b-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-226">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-228">203</span><span class="sxs-lookup"><span data-stu-id="6dc3b-228">203</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-229">130</span><span class="sxs-lookup"><span data-stu-id="6dc3b-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-230">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-232">128</span><span class="sxs-lookup"><span data-stu-id="6dc3b-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc3b-233">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-235">204</span><span class="sxs-lookup"><span data-stu-id="6dc3b-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc3b-236">Variable</span><span class="sxs-lookup"><span data-stu-id="6dc3b-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6dc3b-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc3b-238">205</span><span class="sxs-lookup"><span data-stu-id="6dc3b-238">205</span></span></p></td>
<td><p><span data-ttu-id="6dc3b-239">204</span><span class="sxs-lookup"><span data-stu-id="6dc3b-239">204</span></span></p></td>
</tr>
</tbody>
</table>

