---
title: Référence des erreurs ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 372219a542f911452f2189e41fc6c29c2f86ff1d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945109"
---
# <a name="ado-error-reference"></a><span data-ttu-id="14a69-102">Référence des erreurs ADO</span><span class="sxs-lookup"><span data-stu-id="14a69-102">ADO error reference</span></span>

<span data-ttu-id="14a69-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14a69-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14a69-p101">La constante **ErrorValueEnum** décrit les valeurs des erreurs ADO. Pour obtenir le listing complet de ces constantes énumérées, notamment les valeurs, consultez l' [Annexe B : Erreurs ADO](appendix-b-ado-errors.md). Cette section analyse les erreurs les plus intéressantes et explique certaines situations susceptibles de les déclencher ou des solutions pour les résoudre. La constante **ErrorValueEnum** et le nombre décimal positif court sont tous deux répertoriés.</span><span class="sxs-lookup"><span data-stu-id="14a69-p101">The **ErrorValueEnum** constant describes the ADO error values. For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md). This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem. Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14a69-108">Numéro</span><span class="sxs-lookup"><span data-stu-id="14a69-108">Number</span></span></p></th>
<th><p><span data-ttu-id="14a69-109">Constante ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="14a69-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="14a69-110">Description/causes possibles</span><span class="sxs-lookup"><span data-stu-id="14a69-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a69-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-113">Le fournisseur n'a pas réussi à effectuer l'opération demandée.</span><span class="sxs-lookup"><span data-stu-id="14a69-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p102">Les arguments ne sont pas du type requis, ils ne figurent pas dans des plages de valeurs acceptables ou sont en conflit. Cette erreur est souvent causée par une erreur typographique dans une instruction SQL SELECT. Un nom de champ ou de table mal orthographié, par exemple, peut générer cette erreur. Elle peut également se produire lorsqu'une table ou un champ appelé dans une instruction SELECT n'existe pas dans le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="14a69-p102">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another. This error is often caused by a typographical error in an SQL SELECT statement. For example, a misspelled field name or table name can generate this error. This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p103">Impossible d'ouvrir un fichier. Un nom de fichier mal orthographié a été spécifié ou un fichier a été déplacé, renommé ou supprimé. Sur un réseau, il se peut que le lecteur soit momentanément inaccessible ou que le trafic réseau empêche une connexion.</span><span class="sxs-lookup"><span data-stu-id="14a69-p103">File could not be opened. A misspelled file name was specified, or a file has been moved, renamed, or deleted. Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p104">Impossible de lire le fichier. Le nom du fichier est incorrect, il est possible que le fichier ait été modifié, supprimé ou endommagé.</span><span class="sxs-lookup"><span data-stu-id="14a69-p104">File could not be read. The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p105">Échec d'écriture dans le fichier. Il est possible que vous ayez fermé un fichier puis tenté d'y écrire, ou que le fichier soit endommagé. Si le fichier se trouve sur un lecteur réseau, des conditions réseau temporaires empêchent peut-être des opérations d'écriture sur un lecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="14a69-p105">Write to file failed. You might have closed a file and then tried to write to it, or the file might be corrupted. If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-136"><strong>BOF</strong> ou <strong>EOF</strong> a la valeur True ou l’enregistrement actif a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="14a69-136">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="14a69-137">L’opération demandée nécessite un enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="14a69-137">Requested operation requires a current record.</span></span> <span data-ttu-id="14a69-138">Une tentative a été effectuée pour mettre à jour des enregistrements à l’aide de <strong>Find</strong> ou <strong>Seek</strong> pour déplacer le pointeur d’enregistrement à l’enregistrement de votre choix.</span><span class="sxs-lookup"><span data-stu-id="14a69-138">An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record.</span></span> <span data-ttu-id="14a69-139">Si l’enregistrement est introuvable, <strong>EOF</strong> aura la valeur True.</span><span class="sxs-lookup"><span data-stu-id="14a69-139">If the record is not found, <strong>EOF</strong> will be True.</span></span> <span data-ttu-id="14a69-140">Cette erreur peut également se produire après l’échec de <strong>AddNew</strong> ou <strong>Supprimer</strong> car il n’existe aucun enregistrement actif lors de l’échouent de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="14a69-140">This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-143">L'opération n'est pas autorisée dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="14a69-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-146">Le fournisseur indiqué est différent de celui utilisé.</span><span class="sxs-lookup"><span data-stu-id="14a69-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p107">L'objet <strong>Connection</strong> ne peut pas être fermé explicitement au cours d'une transaction. Les objets <strong>Recordset</strong> ou <strong>Connection</strong> participant à une transaction ne peuvent pas être fermés. Appelez <strong>RollbackTrans</strong> ou <strong>CommitTrans</strong> avant de fermer ces objets.</span><span class="sxs-lookup"><span data-stu-id="14a69-p107"><strong>Connection</strong> object cannot be explicitly closed while in a transaction. A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed. Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p108">L'objet ou le fournisseur ne sont pas en mesure d'effectuer l'opération demandée. Certaines opérations dépendent d'une version de fournisseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="14a69-p108">The object or provider is not capable of performing the requested operation. Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p109">Aucun élément de la collection ne correspond au nom ou à l'ordinal demandé. Un nom de champ ou de table incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="14a69-p109">Item cannot be found in the collection corresponding to the requested name or ordinal. An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p110">L'objet appartient déjà à la collection. Impossible de l'ajouter. Vous ne pouvez pas ajouter deux fois le même objet à la même collection.</span><span class="sxs-lookup"><span data-stu-id="14a69-p110">Object is already in collection. Cannot append. An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-167">L'objet n'est plus valide.</span><span class="sxs-lookup"><span data-stu-id="14a69-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p111">L'application utilise une valeur incorrecte pour l'opération en cours. Vous avez peut-être fourni une chaîne alors que l'opération exige un flux, par exemple.</span><span class="sxs-lookup"><span data-stu-id="14a69-p111">Application uses a value of the wrong type for the current operation. You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p112">L'opération est interdite lorsque l'objet est fermé. Les objets <strong>Connection</strong> ou <strong>Recordset</strong> ont été fermés. Par exemple, une autre routine a peut-être fermé un objet global. Vous pouvez éviter cette erreur en vérifiant la propriété <strong>State</strong> avant d'exécuter une opération.</span><span class="sxs-lookup"><span data-stu-id="14a69-p112">Operation is not allowed when the object is closed. The <strong>Connection</strong> or <strong>Recordset</strong> has been closed. For example, some other routine might have closed a global object. You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p113">L'opération est interdite lorsque l'objet est ouvert. Vous ne pouvez pas ouvrir un objet déjà ouvert. Vous ne pouvez pas ajouter de champs à un objet <strong>Recordset</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="14a69-p113">Operation is not allowed when the object is open. An object that is open cannot be opened. Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-185">Impossible de trouver un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="14a69-185">Provider cannot be found.</span></span> <span data-ttu-id="14a69-186">Il ne peut pas être correctement installé.</span><span class="sxs-lookup"><span data-stu-id="14a69-186">It may not be properly installed.</span></span> <span data-ttu-id="14a69-187">Il est possible que le nom du fournisseur spécifié soit incorrect, qu'il ne soit pas installé sur l'ordinateur exécutant votre code ou que l'installation ait été endommagée.</span><span class="sxs-lookup"><span data-stu-id="14a69-187">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p115">La propriété <strong>ActiveConnection</strong> d'un objet <strong>Recordset</strong>, dont la source est l'objet <strong>Command</strong>, ne peut pas être modifiée. L'application a tenté d'affecter un nouvel objet <strong>Connection</strong> à un objet <strong>Recordset</strong> dont la source est un objet <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="14a69-p115">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed. The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p116">Objet <strong>Parameter</strong> défini de manière incorrecte. Des informations incohérentes ou incomplètes ont été fournies.</span><span class="sxs-lookup"><span data-stu-id="14a69-p116"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p117">Cette opération ne peut utiliser la connexion. Dans ce contexte, elle est soit fermée, soit non valide.</span><span class="sxs-lookup"><span data-stu-id="14a69-p117">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p118">L'opération ne peut pas être exécutée pendant le traitement d'un événement. Une opération ne peut pas effectuée dans un gestionnaire d'événements si elle déclenche à nouveau l'événement. Par exemple, les méthodes de navigation ne doivent pas être appelées dans un gestionnaire d'événements <strong>WillMove</strong>.</span><span class="sxs-lookup"><span data-stu-id="14a69-p118">Operation cannot be performed while processing event. An operation cannot be performed within an event handler that causes the event to fire again. For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-207">Opération impossible avec une exécution asynchrone.</span><span class="sxs-lookup"><span data-stu-id="14a69-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p119">L'utilisateur a annulé l'opération. L'application a appelé la méthode <strong>CancelUpdate</strong> ou <strong>CancelBatch</strong> et l'opération en cours a été annulée.</span><span class="sxs-lookup"><span data-stu-id="14a69-p119">Operation has been canceled by the user. The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-214">L'opération est impossible lors d'une connexion asynchrone.</span><span class="sxs-lookup"><span data-stu-id="14a69-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-217">La transaction de coordination n'est pas valide ou n'a pas été lancée.</span><span class="sxs-lookup"><span data-stu-id="14a69-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-220">L'opération ne peut s'effectuer que si elle est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="14a69-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-223">Les paramètres de sécurité de cet ordinateur interdisent l'accès à une source de données située sur un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="14a69-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p120">Pour usage interne uniquement. Utilisation interdite. (L'entrée a été incluse dans un souci d'exhaustivité. Cette erreur ne doit pas s'afficher dans votre code.)</span><span class="sxs-lookup"><span data-stu-id="14a69-p120">For internal use only. Don't use. (Entry was included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p121">Pour usage interne uniquement. Utilisation interdite. (L'entrée a été incluse dans un souci d'exhaustivité. Cette erreur ne doit pas s'afficher dans votre code.)</span><span class="sxs-lookup"><span data-stu-id="14a69-p121">For internal use only. Don't use. (Entry included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p122">Il existe un conflit entre la valeur des données et les contraintes d'intégrité du champ. Une nouvelle valeur pour l'objet <strong>Field</strong> entraîne la création d'une clé en double. Il se peut qu'une valeur représentant un côté d'une relation entre deux enregistrements ne puisse pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="14a69-p122">Data value conflicts with the integrity constraints of the field. A new value for a <strong>Field</strong> would cause a duplicate key. A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p123">Il est impossible d'écrire dans un champ en raison d'autorisations insuffisantes. L'utilisateur nommé dans la chaîne de connexion ne dispose pas des autorisations nécessaires pour écrire dans un objet <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="14a69-p123">Insufficient permission prevents writing to the field. The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p124">La valeur des données est trop élevée pour être représentée par le type de données du champ. La valeur numérique affectée au champ prévu est trop élevée. Par exemple, une valeur d'entier de type Long a été affectée à un champ d'entier de type Short.</span><span class="sxs-lookup"><span data-stu-id="14a69-p124">Data value is too large to be represented by the field data type. A numeric value that is too large for the intended field was assigned. For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p125">Il existe un conflit entre la valeur des données et le type de données ou les contraintes du champ. Le magasin de données a des contraintes de validation différentes de la valeur de l'objet <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="14a69-p125">Data value conflicts with the data type or constraints of the field. The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-256">La conversion a échoué car la valeur de donnée était signée alors que le type de données du champ utilisé par le fournisseur ne l'était pas.</span><span class="sxs-lookup"><span data-stu-id="14a69-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p126">La valeur de donnée ne peut être convertie pour des raisons autres qu'une incompatibilité de signes ou un débordement de données. Par exemple, la conversion aurait tronqué les données.</span><span class="sxs-lookup"><span data-stu-id="14a69-p126">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-263">La valeur de donnée ne peut être définie ou extraite car le type de données du champ était inconnu, ou le fournisseur ne disposait pas des ressources nécessaires pour effectuer l'opération.</span><span class="sxs-lookup"><span data-stu-id="14a69-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p127">L'enregistrement ne contient pas ce champ. Un nom de champ incorrect a été spécifié ou un champ n'appartenant pas à la collection <strong>Fields</strong> de l'enregistrement actif a été référencé.</span><span class="sxs-lookup"><span data-stu-id="14a69-p127">Record does not contain this field. An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-270">L'URL source ou le parent de l'URL de destination n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="14a69-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="14a69-271">Il existe une erreur typographique dans URL source ou de destination.</span><span class="sxs-lookup"><span data-stu-id="14a69-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="14a69-272">Vous devrez peut-être https://mysite/photo/myphoto.jpg lorsque vous au lieu de https://mysite/photos/myphoto.jpg à la place.</span><span class="sxs-lookup"><span data-stu-id="14a69-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="14a69-273">L’erreur typographique dans l’URL parent (dans ce cas, la <em>photo</em> au lieu de <em>photos</em>) a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="14a69-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p129">Les autorisations sont insuffisantes pour accéder à l'arborescence ou à la sous-arborescence. L'utilisateur nommé dans la chaîne de connexion ne dispose pas des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="14a69-p129">Permissions are insufficient to access tree or subtree. The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p130">L'URL contient des caractères non valides. Assurez-vous que l'URL entrée est correcte. L'URL suit le schéma inscrit pour le fournisseur actuel (par exemple, le schéma de communication http est inscrit pour le fournisseur de publication Internet).</span><span class="sxs-lookup"><span data-stu-id="14a69-p130">URL contains invalid characters. Make sure the URL is typed correctly. The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p131">L'objet représenté par l'URL spécifiée est verrouillé par un ou plusieurs autres processus. Attendez la fin du processus et retentez l'opération. L'objet, auquel vous essayez d'accéder, a été verrouillé par un autre utilisateur ou par un autre processus dans votre application. Cette situation est plus fréquente dans un environnement multi-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14a69-p131">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again. The object you are trying to access has been locked by another user or by another process in your application. This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p132">Impossible d'effectuer l'opération de copie. L'objet nommé par l'URL de destination existe déjà. Spécifiez <strong>adCopyOverwrite</strong> pour remplacer l'objet. Si vous ne spécifiez pas <strong>adCopyOverwrite</strong> en copiant les fichiers dans un répertoire, la copie échoue lorsque vous essayez de copier un élément qui existe déjà dans l'emplacement de destination.</span><span class="sxs-lookup"><span data-stu-id="14a69-p132">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object. If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p133">Le serveur ne peut pas achever l'opération en raison des autres opérations en cours d'exécution ou d'un manque de ressources.</span><span class="sxs-lookup"><span data-stu-id="14a69-p133">The server cannot complete the operation. This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p134">Le fournisseur ne peut pas localiser le périphérique de stockage indiqué par l'URL. Vérifiez que l'URL indiquée est correcte. Cette erreur peut être générée par une URL du périphérique de stockage incorrecte ou d'autres raisons. Il est possible que le périphérique soit déconnecté ou que le trafic réseau empêche la connexion.</span><span class="sxs-lookup"><span data-stu-id="14a69-p134">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly. The URL of the storage device might be incorrect, but this error can occur for other reasons. The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p135">L'opération ne peut pas être effectuée. Le fournisseur ne peut pas obtenir un espace de stockage suffisant. La mémoire RAM ou l'espace disque du serveur sont peut-être insuffisants pour les fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="14a69-p135">Operation cannot be performed. Provider cannot obtain enough storage space. There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-312">L'URL source ou de destination est en dehors de l'étendue de l'enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="14a69-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p136">L'opération a échoué et l'état n'est pas disponible. Il se peut que le champ ne soit pas accessible ou que l'opération n'ait pas été lancée. Un autre utilisateur peut avoir modifié ou supprimé le champ auquel vous tentez d'accéder.</span><span class="sxs-lookup"><span data-stu-id="14a69-p136">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted. Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p137">L'enregistrement nommé par cette URL n'existe pas. Lorsque vous essayez d'ouvrir un fichier à l'aide d'un objet <strong>Record</strong>, le nom du fichier ou son chemin d'accès a été mal orthographié.</span><span class="sxs-lookup"><span data-stu-id="14a69-p137">Record named by this URL does not exist. While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-324">L'URL de l'objet à supprimer ne fait pas partie de l'étendue de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="14a69-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-327">L'opération requiert un <strong>ParentCatalog</strong> valide.</span><span class="sxs-lookup"><span data-stu-id="14a69-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p138">La connexion a été refusée. La nouvelle connexion que vous avez demandée possède d'autres caractéristiques que la connexion en cours.</span><span class="sxs-lookup"><span data-stu-id="14a69-p138">Connection was denied. The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-334">Échec de la mise à jour des champs.</span><span class="sxs-lookup"><span data-stu-id="14a69-334">Fields update failed.</span></span> <span data-ttu-id="14a69-335">Pour plus d’informations, examinez la propriété <strong>Status</strong> des objets field individuels.</span><span class="sxs-lookup"><span data-stu-id="14a69-335">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span> <span data-ttu-id="14a69-336">Cette erreur peut se produire dans deux cas : lorsque vous modifiez la valeur d’un objet <strong>Field</strong> en cours de modification ou ajout d’un enregistrement à la base de données ; et lorsque vous modifiez les propriétés de l’objet <strong>Field</strong> lui-même.</span><span class="sxs-lookup"><span data-stu-id="14a69-336">This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself.</span></span> <span data-ttu-id="14a69-337">La mise à jour de l’objet <strong>Record</strong> ou <strong>Recordset</strong> a échoué en raison d’un problème avec l’un des champs de l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="14a69-337">The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record.</span></span> <span data-ttu-id="14a69-338">Énumérer la collection <strong>Fields</strong> et vérifiez la propriété <strong>Status</strong> de chaque champ pour déterminer la cause du problème.</span><span class="sxs-lookup"><span data-stu-id="14a69-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a69-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p140">Le fournisseur ne prend pas en charge les restrictions de partage. Une restriction de partage des fichiers a été tentée et votre fournisseur ne prend pas en charge ce concept.</span><span class="sxs-lookup"><span data-stu-id="14a69-p140">Provider does not support sharing restrictions. An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a69-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="14a69-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="14a69-p141">Le fournisseur ne prend pas en charge le type demandé de restriction de partage. Une restriction de partage des fichiers d'un type particulier, non prise en charge par votre fournisseur a été tentée. Consultez la documentation du fournisseur pour connaître les restrictions de partage des fichiers prises en charge.</span><span class="sxs-lookup"><span data-stu-id="14a69-p141">Provider does not support the requested kind of sharing restriction. An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider. See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

