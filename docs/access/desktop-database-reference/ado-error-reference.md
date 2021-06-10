---
title: Référence des erreurs ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283393"
---
# <a name="ado-error-reference"></a>Référence des erreurs ADO

**S’applique à** : Access 2013, Office 2013

La constante **ErrorValueEnum** décrit les valeurs des erreurs ADO. Pour obtenir le listing complet de ces constantes énumérées, notamment les valeurs, consultez l' [Annexe B : Erreurs ADO](appendix-b-ado-errors.md). Cette section analyse les erreurs les plus intéressantes et explique certaines situations susceptibles de les déclencher ou des solutions pour les résoudre. La constante **ErrorValueEnum** et le nombre décimal positif court sont tous deux répertoriés.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Constante ErrorValueEnum</p></th>
<th><p>Description/causes possibles</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>Le fournisseur n'a pas pu effectuer l'opération demandée.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Les arguments ne sont pas du type requis, ils ne figurent pas dans des plages de valeurs acceptables ou sont en conflit. Cette erreur est souvent causée par une erreur typographique dans une instruction SQL SELECT. Un nom de champ ou de table mal orthographié, par exemple, peut générer cette erreur. Elle peut également se produire lorsqu'une table ou un champ appelé dans une instruction SELECT n'existe pas dans le magasin de données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>Impossible d'ouvrir un fichier. Un nom de fichier mal orthographié a été spécifié ou un fichier a été déplacé, renommé ou supprimé. Sur un réseau, il se peut que le lecteur soit momentanément inaccessible ou que le trafic réseau empêche une connexion.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>Impossible de lire le fichier. Le nom du fichier est incorrect, il est possible que le fichier ait été modifié, supprimé ou endommagé.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Échec d'écriture dans le fichier. Il est possible que vous ayez fermé un fichier puis tenté d'y écrire, ou que le fichier soit endommagé. Si le fichier se trouve sur un lecteur réseau, des conditions réseau temporaires empêchent peut-être des opérations d'écriture sur un lecteur réseau.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p><strong>BOF</strong> ou <strong>EOF</strong> est égal à True ou l'enregistrement actuel a été supprimé. L'opération demandée nécessite un enregistrement actuel. Une mise à jour des enregistrements a été tentée à l'aide de la méthode <strong>Find</strong> ou <strong>Seek</strong> pour déplacer le pointeur sur l'enregistrement souhaité. Si l'enregistrement est introuvable, <strong>EOF</strong> aura la valeur True. Cette erreur peut se produire après l'échec de <strong>AddNew</strong> ou <strong>Delete</strong> car il n'y a pas d'enregistrement actif en cas d'échec de ces méthodes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>L'opération est interdite dans ce contexte.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>Le fournisseur proposé est différent du fournisseur en cours d'utilisation.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>L'objet <strong>Connection</strong> ne peut pas être fermé explicitement au cours d'une transaction. Les objets <strong>Recordset</strong> ou <strong>Connection</strong> participant à une transaction ne peuvent pas être fermés. Appelez <strong>RollbackTrans</strong> ou <strong>CommitTrans</strong> avant de fermer ces objets.</p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>L'objet ou le fournisseur ne sont pas en mesure d'effectuer l'opération demandée. Certaines opérations dépendent d'une version de fournisseur spécifique.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>Aucun élément de la collection ne correspond au nom ou à l'ordinal demandé. Un nom de champ ou de table incorrect a été spécifié.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>L'objet appartient déjà à la collection. Impossible de l'ajouter. Vous ne pouvez pas ajouter deux fois le même objet à la même collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>L'objet n'est plus valide.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>L'application utilise une valeur incorrecte pour l'opération en cours. Vous avez peut-être fourni une chaîne alors que l'opération exige un flux, par exemple.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>L'opération est interdite lorsque l'objet est fermé. Les objets <strong>Connection</strong> ou <strong>Recordset</strong> ont été fermés. Par exemple, une autre routine a peut-être fermé un objet global. Vous pouvez éviter cette erreur en vérifiant la propriété <strong>State</strong> avant d'exécuter une opération.</p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>L'opération est interdite lorsque l'objet est ouvert. Vous ne pouvez pas ouvrir un objet déjà ouvert. Vous ne pouvez pas ajouter de champs à un objet <strong>Recordset</strong> ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>Fournisseur introuvable. Son installation est peut-être incorrecte. Il est possible que le nom du fournisseur spécifié soit incorrect, qu'il ne soit pas installé sur l'ordinateur exécutant votre code ou que l'installation ait été endommagée.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>La propriété <strong>ActiveConnection</strong> d'un objet <strong>Recordset</strong>, dont la source est l'objet <strong>Command</strong>, ne peut pas être modifiée. L'application a tenté d'affecter un nouvel objet <strong>Connection</strong> à un objet <strong>Recordset</strong> dont la source est un objet <strong>Command</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>Objet <strong>Parameter</strong> défini de manière incorrecte. Des informations incohérentes ou incomplètes ont été fournies.</p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>Cette opération ne peut utiliser la connexion. Dans ce contexte, elle est soit fermée, soit non valide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>L'opération ne peut pas être exécutée pendant le traitement d'un événement. Une opération ne peut pas effectuée dans un gestionnaire d'événements si elle déclenche à nouveau l'événement. Par exemple, les méthodes de navigation ne doivent pas être appelées dans un gestionnaire d'événements <strong>WillMove</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>L'opération est impossible lors d'une exécution asynchrone.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>L'utilisateur a annulé l'opération. L'application a appelé la méthode <strong>CancelUpdate</strong> ou <strong>CancelBatch</strong> et l'opération en cours a été annulée.</p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>L'opération est impossible lors d'une connexion asynchrone.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>La transaction de coordination n'est pas valide ou elle n'a pas démarré.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>L'opération est impossible sans exécution.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>Les paramètres de sécurité de cet ordinateur empêchent d'accéder à une source de données d'un autre domaine.</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>Pour usage interne uniquement. Utilisation interdite. (L'entrée a été incluse dans un souci d'exhaustivité. Cette erreur ne doit pas s'afficher dans votre code.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>Pour usage interne uniquement. Utilisation interdite. (L'entrée a été incluse dans un souci d'exhaustivité. Cette erreur ne doit pas s'afficher dans votre code.)</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>Il existe un conflit entre la valeur des données et les contraintes d'intégrité du champ. Une nouvelle valeur pour l'objet <strong>Field</strong> entraîne la création d'une clé en double. Il se peut qu'une valeur représentant un côté d'une relation entre deux enregistrements ne puisse pas être mise à jour.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>Il est impossible d'écrire dans un champ en raison d'autorisations insuffisantes. L'utilisateur nommé dans la chaîne de connexion ne dispose pas des autorisations nécessaires pour écrire dans un objet <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>La valeur des données est trop élevée pour être représentée par le type de données du champ. La valeur numérique affectée au champ prévu est trop élevée. Par exemple, une valeur d'entier de type Long a été affectée à un champ d'entier de type Short.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>Il existe un conflit entre la valeur des données et le type de données ou les contraintes du champ. Le magasin de données a des contraintes de validation différentes de la valeur de l'objet <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>La conversion a échoué car la valeur des données a été signée, à la différence du type de données de champ utilisé par le fournisseur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>La valeur de donnée ne peut être convertie pour des raisons autres qu'une incompatibilité de signes ou un débordement de données. Par exemple, la conversion aurait tronqué les données.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>La valeur des données ne peut pas être définie ou extraite car le type des données de champ est inconnu ou le fournisseur manque de ressources pour effectuer l'opération.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>L'enregistrement ne contient pas ce champ. Un nom de champ incorrect a été spécifié ou un champ n'appartenant pas à la collection <strong>Fields</strong> de l'enregistrement actif a été référencé.</p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>L’URL source ou le parent de l’URL de destination n’existent pas. Un erreur typographique figure dans l’URL source ou l’URL de destination. Vous https://mysite/photo/myphoto.jpg l’avez peut-être déjà https://mysite/photos/myphoto.jpg fait à la place. L’erreur typographique dans l’URL parent (dans ce cas, il s’agit de <em>photo</em> au lieu de <em>photos</em>) est à l’origine de l’erreur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>Les autorisations sont insuffisantes pour accéder à l'arborescence ou à la sous-arborescence. L'utilisateur nommé dans la chaîne de connexion ne dispose pas des autorisations appropriées.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>L'URL contient des caractères non valides. Assurez-vous que l'URL entrée est correcte. L'URL suit le schéma inscrit pour le fournisseur actuel (par exemple, le schéma de communication http est inscrit pour le fournisseur de publication Internet).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>L'objet représenté par l'URL spécifiée est verrouillé par un ou plusieurs autres processus. Attendez la fin du processus et retentez l'opération. L'objet, auquel vous essayez d'accéder, a été verrouillé par un autre utilisateur ou par un autre processus dans votre application. Cette situation est plus fréquente dans un environnement multi-utilisateur.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>Impossible d'effectuer l'opération de copie. L'objet nommé par l'URL de destination existe déjà. Spécifiez <strong>adCopyOverwrite</strong> pour remplacer l'objet. Si vous ne spécifiez pas <strong>adCopyOverwrite</strong> en copiant les fichiers dans un répertoire, la copie échoue lorsque vous essayez de copier un élément qui existe déjà dans l'emplacement de destination.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>Le serveur ne peut pas achever l'opération en raison des autres opérations en cours d'exécution ou d'un manque de ressources.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>Le fournisseur ne peut pas localiser le périphérique de stockage indiqué par l'URL. Vérifiez que l'URL indiquée est correcte. Cette erreur peut être générée par une URL du périphérique de stockage incorrecte ou d'autres raisons. Il est possible que le périphérique soit déconnecté ou que le trafic réseau empêche la connexion.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>L'opération ne peut pas être effectuée. Le fournisseur ne peut pas obtenir un espace de stockage suffisant. La mémoire RAM ou l'espace disque du serveur sont peut-être insuffisants pour les fichiers temporaires.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>L'URL source ou l'URL de destination ne fait pas partie de l'étendue de l'enregistrement actif.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>L'opération a échoué et l'état n'est pas disponible. Il se peut que le champ ne soit pas accessible ou que l'opération n'ait pas été lancée. Un autre utilisateur peut avoir modifié ou supprimé le champ auquel vous tentez d'accéder.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>L'enregistrement nommé par cette URL n'existe pas. Lorsque vous essayez d'ouvrir un fichier à l'aide d'un objet <strong>Record</strong>, le nom du fichier ou son chemin d'accès a été mal orthographié.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>L'URL de l'objet à supprimer ne fait pas partie de l'étendue de l'enregistrement actif.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>L'opération exige un objet <strong>ParentCatalog</strong> valide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>La connexion a été refusée. La nouvelle connexion que vous avez demandée possède d'autres caractéristiques que la connexion en cours.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>Échec de la mise à jour des champs. Pour plus d'informations, examinez la propriété <strong>Status</strong> des objets Field individuels. Cette erreur peut se produire dans deux cas : premièrement, lors de la modification d'une valeur d'un objet <strong>Field</strong> au cours de la modification ou de l'ajout d'un enregistrement dans la base de données ; deuxièmement, lors de la modification des propriétés de l'objet <strong>Field</strong> lui-même. La mise à jour de l'objet <strong>Record</strong> ou <strong>Recordset</strong> a échoué à cause d'un problème lié à un des champs dans l'enregistrement actif. Énumérez la collection <strong>Fields</strong> et vérifiez la propriété <strong>Status</strong> de chaque champ pour déterminer la cause du problème.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>Le fournisseur ne prend pas en charge les restrictions de partage. Une restriction de partage des fichiers a été tentée et votre fournisseur ne prend pas en charge ce concept.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>Le fournisseur ne prend pas en charge le type demandé de restriction de partage. Une restriction de partage des fichiers d'un type particulier, non prise en charge par votre fournisseur a été tentée. Consultez la documentation du fournisseur pour connaître les restrictions de partage des fichiers prises en charge.</p></td>
</tr>
</tbody>
</table>

