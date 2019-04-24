---
title: Connection. OpenRecordset, méthode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abbb7a4f58714aef0e085d0f37b5ee49378e0f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295848"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="ea997-102">Connection. OpenRecordset, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="ea997-102">Connection.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="ea997-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea997-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea997-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ea997-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea997-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea997-105">Syntax</span></span>

<span data-ttu-id="ea997-106">*expression* . OpenRecordset (***Name***, ***type***, ***options***, ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="ea997-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="ea997-107">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="ea997-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea997-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea997-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea997-109">Nom</span><span class="sxs-lookup"><span data-stu-id="ea997-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ea997-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="ea997-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ea997-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ea997-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ea997-112">Description</span><span class="sxs-lookup"><span data-stu-id="ea997-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea997-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ea997-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ea997-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ea997-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ea997-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ea997-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ea997-p101">Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.  </span><span class="sxs-lookup"><span data-stu-id="ea997-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea997-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="ea997-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="ea997-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ea997-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea997-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ea997-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ea997-122">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ea997-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="ea997-123"><strong>Remarque</strong>: Si vous ouvrez un <strong>objet Recordset</strong> dans un espace de travail Microsoft Access et que vous ne spécifiez pas de type, <strong>OpenRecordset</strong> crée un <strong>objet Recordset</strong>de type table, si possible.</span><span class="sxs-lookup"><span data-stu-id="ea997-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="ea997-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea997-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea997-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="ea997-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="ea997-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ea997-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea997-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ea997-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ea997-128">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea997-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="ea997-129"><strong>Remarque</strong>: les constantes <strong>dbConsistent</strong> et <strong>dbInconsistent</strong> s'excluent mutuellement et l'utilisation des deux déclenche une erreur.</span><span class="sxs-lookup"><span data-stu-id="ea997-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="ea997-130">Fournir un argument LockEdits lorsque les options utilisent la constante <strong>DBReadOnly</strong> génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="ea997-130">Supplying a lockedits argument when options use the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea997-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="ea997-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="ea997-132">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ea997-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea997-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ea997-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ea997-134">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea997-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="ea997-135"><strong>Remarque</strong>: vous pouvez utiliser <strong>DBReadOnly</strong> dans l'argument options ou LockEdits, mais pas dans les deux.</span><span class="sxs-lookup"><span data-stu-id="ea997-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="ea997-136">If you use it for both arguments, a run-time error occurs.</span><span class="sxs-lookup"><span data-stu-id="ea997-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ea997-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ea997-137">Return value</span></span>

<span data-ttu-id="ea997-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="ea997-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="ea997-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea997-139">Remarks</span></span>

<span data-ttu-id="ea997-p105">En général, si l'utilisateur obtient cette erreur lors de la mise à jour d'un enregistrement, le code peut actualiser le contenu des champs et extraire les valeurs qui viennent d'être modifiées. Si l'erreur se produit lors de la suppression d'un enregistrement, le code peut afficher les nouvelles données de l'enregistrement pour l'utilisateur et un message indique que les données ont été modifiées dernièrement. À ce niveau, le code peut demander une confirmation que l'utilisateur souhaite encore supprimer l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ea997-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="ea997-143">Vous devez également utiliser la constante **dbSeeChanges** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté à un moteur de base de données Microsoft Access dans une table Microsoft SQL Server 6.0 (ou version ultérieure) possédant une colonne IDENTITY, autrement une erreur peut être générée.</span><span class="sxs-lookup"><span data-stu-id="ea997-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="ea997-p106">L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **MoveLast** dès que l'objet **Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="ea997-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="ea997-146">Si vous fermez un objet **Recordset** avec la méthode **[Close](connection-close-method-dao.md)**, l'objet est automatiquement supprimé de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ea997-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="ea997-147">Si *source* fait référence à une instruction SQL composée d'une chaîne concaténée avec une valeur non entière, et que les paramètres système spécifient un caractère non-U. S. Decimal tel qu'une virgule (par exemple, strSQL = &gt; " &amp; Price" lngPrice et lngPrice = 125, 50), une erreur se produit lorsque vous essayez d'ouvrir l' **objet Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ea997-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="ea997-148">Cela s'explique par le fait que lors de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut du système et le langage SQL n'accepte que les caractères décimaux de la notation américaine.</span><span class="sxs-lookup"><span data-stu-id="ea997-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


