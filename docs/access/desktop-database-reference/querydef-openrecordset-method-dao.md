---
title: Méthode QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710243"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="ae941-102">Méthode QueryDef.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae941-102">QueryDef.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="ae941-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae941-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae941-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ae941-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae941-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae941-105">Syntax</span></span>

<span data-ttu-id="ae941-106">*expression* . OpenRecordset (***Type***, ***Options***, ***VerrouillerModification***)</span><span class="sxs-lookup"><span data-stu-id="ae941-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="ae941-107">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="ae941-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae941-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae941-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae941-109">Nom</span><span class="sxs-lookup"><span data-stu-id="ae941-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ae941-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="ae941-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ae941-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ae941-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ae941-112">Description</span><span class="sxs-lookup"><span data-stu-id="ae941-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae941-113"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="ae941-113"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="ae941-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ae941-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="ae941-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ae941-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ae941-116">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ae941-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="ae941-117"><strong>Remarque</strong>: Si vous ouvrez un <STRONG>objet Recordset</STRONG> dans un espace de travail Microsoft Access et que vous ne spécifiez pas un type, <STRONG>OpenRecordset</STRONG> crée un <STRONG>objet Recordset</STRONG>de type table, si possible.</span><span class="sxs-lookup"><span data-stu-id="ae941-117"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="ae941-118">Si vous spécifiez une table liée ou une requête, <STRONG>OpenRecordset</STRONG> crée un <STRONG>jeu d’enregistrements</STRONG>de type feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="ae941-118">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae941-119"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="ae941-119"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="ae941-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ae941-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ae941-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ae941-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ae941-122">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae941-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="ae941-123"><strong>Remarque</strong>: l’une des constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement, et les deux entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="ae941-123"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="ae941-124">Fournir un argument lockedits lorsque options utilise la constante <STRONG>peut entraîner</STRONG> génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="ae941-124">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae941-125"><em>VerrouillerModification</em></span><span class="sxs-lookup"><span data-stu-id="ae941-125"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="ae941-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ae941-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="ae941-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ae941-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ae941-128">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae941-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="ae941-129"><strong>Remarque</strong>: vous pouvez utiliser <STRONG>peut entraîner</STRONG> dans l’argument options ou l’argument lockedits, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="ae941-129"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="ae941-130">Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="ae941-130">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ae941-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae941-131">Return value</span></span>

<span data-ttu-id="ae941-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="ae941-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="ae941-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae941-133">Remarks</span></span>

<span data-ttu-id="ae941-134">Vous devez également utiliser la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté à un moteur de base de données Microsoft Access dans une table Microsoft SQL Server 6.0 (ou version ultérieure) possédant une colonne IDENTITY, autrement une erreur peut être générée.</span><span class="sxs-lookup"><span data-stu-id="ae941-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="ae941-p104">L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **[MoveLast](recordset-movelast-method-dao.md)** dès que l'objet **Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="ae941-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="ae941-137">Si vous fermez un objet **Recordset** avec la méthode **Close**, l'objet est automatiquement supprimé de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="ae941-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="ae941-138">Si *la source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="ae941-138">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="ae941-139">Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="ae941-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


