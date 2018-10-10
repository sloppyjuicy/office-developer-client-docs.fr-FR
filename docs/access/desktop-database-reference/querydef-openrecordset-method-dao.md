---
title: QueryDef.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50d31adf61df0848a22c9c22f229b22c7992d913
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469626"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="58802-102">QueryDef.OpenRecordset Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="58802-102">QueryDef.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="58802-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="58802-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="58802-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="58802-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="58802-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58802-105">Syntax</span></span>

<span data-ttu-id="58802-106">*expression* . OpenRecordset (***Type***, ***Options***, ***VerrouillerModification***)</span><span class="sxs-lookup"><span data-stu-id="58802-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="58802-107">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="58802-107">*expression* A variable that represents a **QueryDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="58802-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58802-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58802-109">Name</span><span class="sxs-lookup"><span data-stu-id="58802-109">Name</span></span></p></th>
<th><p><span data-ttu-id="58802-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="58802-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="58802-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="58802-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="58802-112">Description</span><span class="sxs-lookup"><span data-stu-id="58802-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58802-113">Type</span><span class="sxs-lookup"><span data-stu-id="58802-113">Type</span></span></p></td>
<td><p><span data-ttu-id="58802-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="58802-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="58802-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="58802-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="58802-116">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="58802-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="58802-p101">Si vous ouvrez un <STRONG>Recordset</STRONG> dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, <STRONG>OpenRecordset</STRONG> crée un <STRONG>Recordset</STRONG> de type table, si possible. Si vous spécifiez une table liée ou une requête, <STRONG>OpenRecordset</STRONG> crée un <STRONG>Recordset</STRONG> de type feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="58802-p101">If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58802-119">Options</span><span class="sxs-lookup"><span data-stu-id="58802-119">Options</span></span></p></td>
<td><p><span data-ttu-id="58802-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="58802-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="58802-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="58802-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="58802-122">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="58802-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="58802-p102">Les constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement, et l’utilisation de ces deux constantes peut entraîner une erreur. L’indication d’un argument lockedits lorsque options utilise la constante <STRONG>dbReadOnly</STRONG> génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="58802-p102">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></P>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58802-125">VerrouillerModification</span><span class="sxs-lookup"><span data-stu-id="58802-125">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="58802-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="58802-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="58802-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="58802-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="58802-128">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="58802-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="58802-p103">Vous pouvez utiliser <STRONG>dbReadOnly</STRONG> dans l’argument options ou l’argument lockededits, mais pas dans les deux. Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="58802-p103">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span></P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="58802-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58802-131">Return Value</span></span>

<span data-ttu-id="58802-132">Recordset</span><span class="sxs-lookup"><span data-stu-id="58802-132">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="58802-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="58802-133">Remarks</span></span>

<span data-ttu-id="58802-134">Vous devez également utiliser la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté à un moteur de base de données Microsoft Access dans une table Microsoft SQL Server 6.0 (ou version ultérieure) possédant une colonne IDENTITY, autrement une erreur peut être générée.</span><span class="sxs-lookup"><span data-stu-id="58802-134">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="58802-p104">L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **[MoveLast](recordset-movelast-method-dao.md)** dès que l'objet **Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="58802-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="58802-137">Si vous fermez un objet **Recordset** avec la méthode **Close**, l'objet est automatiquement supprimé de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="58802-137">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="58802-138">Si <EM>la source</EM> fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le <STRONG>jeu d’enregistrements</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="58802-138">If <EM>source</EM> refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="58802-139">Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="58802-139">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span></P>


