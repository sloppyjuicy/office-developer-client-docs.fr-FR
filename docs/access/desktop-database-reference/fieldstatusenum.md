---
title: FieldStatusEnum (référence de base de données de bureau Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ccf98f2a740e2a077d6e2451102bfc72bcd1b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292516"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="0cb7a-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="0cb7a-102">FieldStatusEnum</span></span>

<span data-ttu-id="0cb7a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cb7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0cb7a-104">Spécifie l'état d'un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="0cb7a-105">Les valeurs **adFieldPending\*** indiquent l'opération à l'origine de l'état ; elles peuvent être combinées avec d'autres valeurs d'état.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0cb7a-106">Constante</span><span class="sxs-lookup"><span data-stu-id="0cb7a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="0cb7a-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cb7a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="0cb7a-108">Description</span><span class="sxs-lookup"><span data-stu-id="0cb7a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-110">27</span><span class="sxs-lookup"><span data-stu-id="0cb7a-110">26</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-111">Indique que le champ spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-113">an</span><span class="sxs-lookup"><span data-stu-id="0cb7a-113">12</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p101">Indique qu’une valeur d’état non valide a été envoyée depuis ADO vers le fournisseur OLE DB. Causes possibles : un fournisseur OLE DB 1.0 ou 1.1, ou une combinaison incorrecte de <a href="value-property-ado.md">Value</a> et <a href="status-property-ado-field.md">Status</a>.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p101">Indicates that an invalid status value was sent from ADO to the OLE DB provider. Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-117">vingtaine</span><span class="sxs-lookup"><span data-stu-id="0cb7a-117">20</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-118">Indique que le serveur de l’URL spécifiée par <a href="source-property-ado-record.md">Source</a> n’a pas pu terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-120">23</span><span class="sxs-lookup"><span data-stu-id="0cb7a-120">23</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-121">Indique que, pendant une opération de déplacement, un arbre ou sous-arbre a été déplacé vers un nouvel emplacement, mais que la source n'a pu être supprimée.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-123">n°2</span><span class="sxs-lookup"><span data-stu-id="0cb7a-123">2</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-124">Indique que l'extraction ou le stockage du champ entraînera une perte de données.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-126">7j/7</span><span class="sxs-lookup"><span data-stu-id="0cb7a-126">7</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-127">Indique que le champ n'a pu être ajouté car le fournisseur a dépassé une limite (par exemple, le nombre de champs permis).</span><span class="sxs-lookup"><span data-stu-id="0cb7a-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-129">6.x</span><span class="sxs-lookup"><span data-stu-id="0cb7a-129">6</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-130">Indique que les données renvoyées par le fournisseur ont débordé le type de données du champ.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-132">kg</span><span class="sxs-lookup"><span data-stu-id="0cb7a-132">13</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-133">Indique que la valeur par défaut du champ a été utilisée lors de la définition des données.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-135">Seiz</span><span class="sxs-lookup"><span data-stu-id="0cb7a-135">16</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-136">Indique que le champ spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-138">0,15</span><span class="sxs-lookup"><span data-stu-id="0cb7a-138">15</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p102">Indique que ce champ a été ignoré lors de la définition des valeurs de données dans la source. Le fournisseur n'a pas défini de valeur.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p102">Indicates that this field was skipped when setting data values in the source. The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-142">10</span><span class="sxs-lookup"><span data-stu-id="0cb7a-142">10</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-143">Indique que le champ ne peut être modifié car il est une entité calculée ou dérivée.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-145">cm</span><span class="sxs-lookup"><span data-stu-id="0cb7a-145">17</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-146">Indique l'URL de la source des données contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-148">3</span><span class="sxs-lookup"><span data-stu-id="0cb7a-148">3</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-149">Indique que le fournisseur a renvoyé une valeur VARIANT de type VT_NULL et que ce champ n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-150"><strong>adFieldOK</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-151">0</span><span class="sxs-lookup"><span data-stu-id="0cb7a-151">0</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p103">Par défaut. Indique que le champ a été ajouté ou supprimé avec succès.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p103">Default. Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-155">22,5</span><span class="sxs-lookup"><span data-stu-id="0cb7a-155">22</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-156">Indique que le fournisseur est incapable d'obtenir suffisamment d'espace de stockage pour mener à bien une opération de déplacement ou de copie.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-158">0x40000</span><span class="sxs-lookup"><span data-stu-id="0cb7a-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p104">Indique soit que le champ a ét supprimé puis à nouveau ajouté, peut-être avec un type de données différent, soit que la valeur du champ a changé (dernier état connu : adFieldOK). La forme finale du champ modifiera la collection <a href="fields-collection-ado.md">Fields</a> après appel de la méthode <a href="update-method-ado.md">Update</a>.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p104">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed. The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-162">0x20000</span><span class="sxs-lookup"><span data-stu-id="0cb7a-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p105">Indique l'opération <strong>Delete</strong> a entraîné la définition de l'état. Le champ a été marqué pour suppression de la collection <strong>Fields</strong> après appel de la méthode <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p105">Indicates that the <strong>Delete</strong> operation caused the status to be set. The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-166">0x10000</span><span class="sxs-lookup"><span data-stu-id="0cb7a-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p106">Indique que l'opération <strong>Append</strong> a entraîné la définition de l'état. <strong>Field</strong> a été marqué pour ajout à la collection <strong>Fields</strong> après appel de la méthode <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p106">Indicates that the <strong>Append</strong> operation caused the status to be set. The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-170">0x80000</span><span class="sxs-lookup"><span data-stu-id="0cb7a-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-171">Indique que le fournisseur ne peut déterminer l'opération qui a défini l'état du champ.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-173">n.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-174">Indique que le fournisseur ne peut déterminer l'opération qui a défini l'état du champ, et que ce dernier sera supprimé de la collection <strong>Fields</strong> après appel de la méthode <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-176">4,9</span><span class="sxs-lookup"><span data-stu-id="0cb7a-176">9</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-177">Indique que le champ ne peut être modifié car il est défini en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-179">heures/24</span><span class="sxs-lookup"><span data-stu-id="0cb7a-179">24</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-180">Indique que le champ de la source de données est défini en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-182">neuf</span><span class="sxs-lookup"><span data-stu-id="0cb7a-182">19</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-183">Indique que le fournisseur n'a pu effectuer l'opération car un objet est déjà présent à l'URL de destination et le fournisseur ne peut l'effacer.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-185">18</span><span class="sxs-lookup"><span data-stu-id="0cb7a-185">18</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-186">Indique que le fournisseur n'a pas pu effectuer l'opération car la source de données est verrouillée par une application ou un processus (ou plusieurs).</span><span class="sxs-lookup"><span data-stu-id="0cb7a-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-188">25</span><span class="sxs-lookup"><span data-stu-id="0cb7a-188">25</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-189">Indique que l'URL source ou de destination est en dehors de l'étendue de l'enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-191">a4</span><span class="sxs-lookup"><span data-stu-id="0cb7a-191">11</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-192">Indique que la valeur a transgressé la contrainte de schéma de la source de données pour le champ.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-194">disque</span><span class="sxs-lookup"><span data-stu-id="0cb7a-194">5</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-195">Indique que la valeur de donnée renvoyée par le fournisseur a été signée, contrairement au type de données de la valeur du champ ADO.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-197">4</span><span class="sxs-lookup"><span data-stu-id="0cb7a-197">4</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-198">Indique que des données de longueur variable ont été tronquées lors de la lecture de la source de données.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb7a-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-200">8bits</span><span class="sxs-lookup"><span data-stu-id="0cb7a-200">8</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-p107">Indique que le fournisseur n'a pu déterminer la valeur lors de la lecture de la source de données. Par exemple, la ligne venait d'être créée, la valeur par défaut de la colonne n'était pas disponible, et une nouvelle valeur n'avait pas encore été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-p107">Indicates that the provider could not determine the value when reading from the data source. For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb7a-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="0cb7a-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb7a-204">21</span><span class="sxs-lookup"><span data-stu-id="0cb7a-204">21</span></span></p></td>
<td><p><span data-ttu-id="0cb7a-205">Indique que le fournisseur est incapable to localiser le volume de stockage indiqué par l'URL.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0cb7a-206">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0cb7a-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="0cb7a-207">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-207">These constants do not have ADO/WFC equivalents.</span></span>

