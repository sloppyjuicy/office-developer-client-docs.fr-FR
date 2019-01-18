---
title: Méthode Recordset2.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706505"
---
# <a name="recordset2openrecordset-method-dao"></a><span data-ttu-id="b2897-102">Méthode Recordset2.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="b2897-102">Recordset2.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="b2897-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2897-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2897-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="b2897-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2897-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2897-105">Syntax</span></span>

<span data-ttu-id="b2897-106">*expression* . OpenRecordset (***Type***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="b2897-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="b2897-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b2897-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2897-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2897-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2897-109">Nom</span><span class="sxs-lookup"><span data-stu-id="b2897-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b2897-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="b2897-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b2897-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="b2897-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b2897-112">Description</span><span class="sxs-lookup"><span data-stu-id="b2897-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2897-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b2897-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b2897-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2897-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b2897-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="b2897-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b2897-p101">Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.  </span><span class="sxs-lookup"><span data-stu-id="b2897-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2897-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="b2897-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="b2897-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b2897-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="b2897-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b2897-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b2897-122">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="b2897-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="b2897-123"><strong>Remarque</strong>: Si vous ouvrez un <STRONG>objet Recordset</STRONG> dans un espace de travail Microsoft Access et que vous ne spécifiez pas un type, <STRONG>OpenRecordset</STRONG> crée un <STRONG>objet Recordset</STRONG>de type table, si possible.</span><span class="sxs-lookup"><span data-stu-id="b2897-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="b2897-124">Si vous spécifiez une table liée ou une requête, <STRONG>OpenRecordset</STRONG> crée un <STRONG>jeu d’enregistrements</STRONG>de type feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="b2897-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2897-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="b2897-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="b2897-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b2897-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="b2897-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b2897-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b2897-128">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2897-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="b2897-129"><strong>Remarque</strong>: l’une des constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement, et les deux entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="b2897-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="b2897-130">Fournir un argument lockedits lorsque options utilise la constante <STRONG>peut entraîner</STRONG> génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="b2897-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2897-131"><em>VerrouillerModification</em></span><span class="sxs-lookup"><span data-stu-id="b2897-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="b2897-132">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b2897-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="b2897-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b2897-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b2897-134">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2897-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="b2897-135"><strong>Remarque</strong>: vous pouvez utiliser <STRONG>peut entraîner</STRONG> dans l’argument options ou l’argument lockedits, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="b2897-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="b2897-136">Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="b2897-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b2897-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2897-137">Return value</span></span>

<span data-ttu-id="b2897-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="b2897-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="b2897-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2897-139">Remarks</span></span>

<span data-ttu-id="b2897-p105">En règle générale, si l'utilisateur obtient cette erreur pendant la mise à jour d'un enregistrement, votre code doit actualiser le contenu des champs et extraire les valeurs nouvellement modifiées. Si l'erreur se produit lors de la suppression d'un enregistrement, votre code doit présenter les nouvelles données de l'enregistrement à l'utilisateur et afficher un message indiquant que les données ont été récemment modifiées. À ce stade, votre code peut demander à l'utilisateur de confirmer sa volonté de supprimer l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b2897-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="b2897-143">Par ailleurs, il est recommandé d'utiliser la constante **dbSeeChanges** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté au moteur de base de données Microsoft Access pour une table Microsoft SQL Server 6.0 (ou version ultérieure) qui comporte une colonne IDENTITY. À défaut, une erreur risque de se produire.</span><span class="sxs-lookup"><span data-stu-id="b2897-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="b2897-p106">L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **MoveLast** dès que l'objet **Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="b2897-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="b2897-146">Le fait de fermer un objet **Recordset** par le biais de la méthode **[Close](connection-close-method-dao.md)** entraîne sa suppression automatique au niveau de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="b2897-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="b2897-147">Si *la source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="b2897-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="b2897-148">Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="b2897-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


