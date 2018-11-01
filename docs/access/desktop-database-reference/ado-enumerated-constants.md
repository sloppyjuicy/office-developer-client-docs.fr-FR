---
title: Constantes énumérées ADO
TOCTitle: ADO Enumerated Constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e9944138dcdca49f33ca293a9bdf41d88d86e9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882307"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="53f7e-102">Constantes énumérées ADO</span><span class="sxs-lookup"><span data-stu-id="53f7e-102">ADO Enumerated Constants</span></span>


<span data-ttu-id="53f7e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53f7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53f7e-p101">Pour faciliter le débogage, les énumérations ADO comportent une valeur pour chaque constante. Cependant, cette valeur est fournie uniquement à titre indicatif et peut changer d'une version d'ADO à une autre. Votre code doit dépendre uniquement du nom et non de la valeur réelle de chaque constante énumérée.</span><span class="sxs-lookup"><span data-stu-id="53f7e-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-107"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-107"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-108">Pour un objet <strong>Recordset</strong> RDS, spécifie la priorité d'exécution du thème asynchrone qui recherche des données.</span><span class="sxs-lookup"><span data-stu-id="53f7e-108">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-109"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-109"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-110">Indique quand le fournisseur <strong>MSDataShape</strong> recalcule les colonnes regroupées et calculées dans un <strong>jeu d’enregistrements</strong>hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="53f7e-110">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-111"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-111"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-112">Indique les champs qui peuvent être utilisés pour détecter les conflits pendant une mise à jour optimiste d'une ligne de la source de données avec un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-112">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-113"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-113"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-114">Indique si la méthode <strong>UpdateBatch</strong> est suivie d'une opération implicite de la méthode <strong>Resync</strong> et, dans ce cas, la portée de cette opération.</span><span class="sxs-lookup"><span data-stu-id="53f7e-114">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-115"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-115"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-116">Indique les enregistrements affectés par une opération.</span><span class="sxs-lookup"><span data-stu-id="53f7e-116">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-117"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-117"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-118">Spécifie un signet indiquant où doit commencer l'opération.</span><span class="sxs-lookup"><span data-stu-id="53f7e-118">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-119"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-119"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-120">Spécifie comment interpréter un argument de commande.</span><span class="sxs-lookup"><span data-stu-id="53f7e-120">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-121"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-121"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-122">Spécifie la position relative de deux enregistrements représentés par leurs signets.</span><span class="sxs-lookup"><span data-stu-id="53f7e-122">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-123"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-123"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-124">Spécifie les autorisations disponibles pour modifier les données dans une <strong>Connexion</strong>, en ouvrant un <strong>Enregistrement</strong>, ou en spécifiant des valeurs pour la propriété <strong>Mode</strong> de l' <strong>Enregistrement</strong> et des objets <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-124">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-125"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-125"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-126">Indique si la méthode <strong>Open</strong> d'un objet <strong>Connection</strong> doit être exécutée après (de façon synchrone) ou avant (de façon asynchrone) l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="53f7e-126">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-127"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-127"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-128">Indique si une boîte de dialogue doit être affichée pour demander les paramètres manquants lors de l'ouverture d'une connexion à une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="53f7e-128">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-129"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-129"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-130">Spécifie le fonctionnement de la méthode <strong>CopyRecord</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-130">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-131"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-131"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-132">Spécifie l'emplacement du moteur de curseur.</span><span class="sxs-lookup"><span data-stu-id="53f7e-132">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-133"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-133"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-134">Spécifie la fonctionnalité que la méthode <strong>Supports</strong> doit tester.</span><span class="sxs-lookup"><span data-stu-id="53f7e-134">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-135"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-135"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-136">Spécifie le type de curseur utilisé dans un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-136">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-137"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-137"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-138">Spécifie le type de données d'un <strong>Champ</strong>, d'un <strong>Paramètre</strong> ou d'une <strong>Propriété</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-138">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-139"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-139"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-140">Spécifie l'état d'édition d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="53f7e-140">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-141"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-141"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-142">Spécifie le type d'erreur d'exécution ADO.</span><span class="sxs-lookup"><span data-stu-id="53f7e-142">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-143"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-143"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-144">Spécifie la cause à l'origine d'un événement.</span><span class="sxs-lookup"><span data-stu-id="53f7e-144">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-145"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-145"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-146">Spécifie l'état en cours de l'exécution d'un événement.</span><span class="sxs-lookup"><span data-stu-id="53f7e-146">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-147"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-147"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-148">Spécifie la manière dont un fournisseur doit exécuter une commande.</span><span class="sxs-lookup"><span data-stu-id="53f7e-148">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-149"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-149"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-150">Spécifie les champs spéciaux référencés dans une collection <strong>Fields</strong> d'un objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-150">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-151"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-151"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-152">Spécifie un ou plusieurs attributs d'un objet <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-152">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-153"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-153"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-154">Spécifie l'état d'un objet <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-154">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-155"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-155"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-156">Spécifie le groupe d'enregistrements à filtrer depuis un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-156">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-157"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-157"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-158">Spécifie le nombre d'enregistrements à extraire depuis un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-158">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-159"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-159"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-160">Spécifie le niveau d'isolement de transaction d'un objet <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-160">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-161"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-161"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-162">Spécifie le caractère utilisé comme séparateur de ligne dans les objets texte <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-162">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-163"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-163"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-164">Spécifie le type de verrouillage appliqué aux enregistrements pendant l'édition.</span><span class="sxs-lookup"><span data-stu-id="53f7e-164">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-165"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-165"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-166">Spécifie les enregistrements qui doivent être renvoyés au serveur.</span><span class="sxs-lookup"><span data-stu-id="53f7e-166">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-167"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-167"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-168">Spécifie le fonctionnement de la méthode <strong>MoveRecord</strong> de l'objet <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="53f7e-168">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-169"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-169"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-170">Indique si un objet est ouvert ou fermé, s'il se connecte à une source de données, s'il exécute une commande ou s'il extrait des données.</span><span class="sxs-lookup"><span data-stu-id="53f7e-170">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-171"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-171"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-172">Spécifie les attributs d'un objet <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-172">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-173"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-173"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-174">Spécifie si l'objet <strong>Parameter</strong> représente un paramètre d'entrée, un paramètre de sortie ou les deux, ou encore si le paramètre correspond à la valeur renvoyée par une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="53f7e-174">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-175"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-175"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-176">Spécifie le format dans lequel enregistrer un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-176">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-177"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-177"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-178">Spécifie la position en cours du pointeur de l'enregistrement dans un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-178">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-179"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-179"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-180">Spécifie les attributs d'un objet <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-180">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-181"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-181"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-182">Indique si un objet <strong>Record</strong> existant doit être ouvert ou si un nouvel objet <strong>Record</strong> doit être créé pour la méthode <strong>Open</strong> de l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-182">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-183"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-183"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-p102">Spécifie les options nécessaires pour ouvrir un objet <strong>Record</strong>. Ces valeurs peuvent être combinées avec un opérateur OR.</span><span class="sxs-lookup"><span data-stu-id="53f7e-p102">Specifies options for opening a <strong>Record</strong>. These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-186"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-186"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-187">Spécifie l'état d'un enregistrement en cas de mise à jour par lots et autres opérations globales de ce type.</span><span class="sxs-lookup"><span data-stu-id="53f7e-187">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-188"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-188"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-189">Spécifie le type de l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-189">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-190"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-190"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-191">Spécifie si les valeurs sous-jacentes sont remplacées par un appel à <strong>Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-191">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-192"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-192"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-p103">Spécifie si un fichier doit être créé ou remplacé en cas de sauvegarde d'un objet <strong>Stream</strong>. Les valeurs peuvent être combinées avec un opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="53f7e-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-195"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-195"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-p104">Spécifie le type d'objet <strong>Recordset</strong> de schéma extrait par la méthode <strong>OpenSchema</strong>. Spécifie le sens de la recherche d'un enregistrement dans un <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-p104">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves. Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-198"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-198"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-199">Spécifie la direction d'une recherche d'enregistrement dans un objet <strong>Recordset</strong> et le type de méthode <strong>Seek</strong> à exécuter.</span><span class="sxs-lookup"><span data-stu-id="53f7e-199">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-200"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-200"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-p105">Spécifie le type de méthode <strong>Seek</strong> à exécuter et les options permettant d'ouvrir un objet <strong>Stream</strong>. Les valeurs peuvent être combinées avec un opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="53f7e-p105">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-203"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-203"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-p106">Spécifie les options permettant d'ouvrir un objet <strong>Stream</strong>. Les valeurs peuvent être combinées avec un opérateur AND. Indique également s'il faut lire l'ensemble du flux ou seulement la ligne suivante d'un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-p106">Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-206"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-206"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-207">Indique s'il faut lire l'ensemble du flux ou seulement la ligne suivante d'un objet <strong>Stream</strong>. Spécifie également le type des données stockées dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-207">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-208"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-208"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-209">Spécifie le type des données stockées dans un objet <strong>Stream</strong>. Indique également si un séparateur de ligne est ajouté à la chaîne écrite dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-209">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-210"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-210"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-211">Indique si un séparateur de ligne est ajouté à la chaîne écrite dans un objet <strong>Stream</strong>. Spécifie également le format à utiliser pour extraire un objet <strong>Recordset</strong> sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="53f7e-211">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53f7e-212"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-212"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-213">Spécifie le format à utiliser pour extraire un objet <strong>Recordset</strong> sous forme de chaîne. Indique également les attributs de transaction d'un objet <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-213">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53f7e-214"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="53f7e-214"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="53f7e-215">Spécifie les attributs de transaction d'un objet <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="53f7e-215">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

