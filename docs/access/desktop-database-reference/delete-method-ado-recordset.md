---
title: Delete, méthode (Recordset ADO)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 73dc83a240cb5e46b1b46e5d8bafbcd6ba1b8d56
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553136"
---
# <a name="delete-method-ado-recordset"></a>Delete, méthode (Recordset ADO)

**S’applique à** : Access 2013, Office 2013

Supprime l'enregistrement actif ou un groupe d'enregistrements.

## <a name="syntax"></a>Syntaxe

*recordset*. Supprimer *AffectRecords*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*AffectRecords* |Valeur [AffectEnum](affectenum.md) qui détermine le nombre d'enregistrements concernés par la méthode **Delete**. La valeur par défaut est **adAffectCurrent**.|

> [!NOTE]
> [!REMARQUE] **adAffectAll** et **adAffectAllChapters** ne sont pas des arguments valides de la méthode **Delete**.

## <a name="remarks"></a>Remarques

L'utilisation de la méthode **Delete** marque pour suppression l'enregistrement actif ou un groupe d'enregistrements d'un objet [Recordset](recordset-object-ado.md). Si l'objet **Recordset** n'autorise pas la suppression d'enregistrements, une erreur se produit. Si vous êtes en mode de mise à jour immédiate, les suppressions sont effectuées immédiatement dans la base de données. S'il est impossible de supprimer un enregistrement (en raison de violations d'intégrité de la base de données, par exemple), l'enregistrement reste en mode édition après l'appel de la méthode **Update**. Cela signifie que vous devez annuler la mise à jour avec [CancelUpdate](cancelupdate-method-ado.md) avant de quitter l'enregistrement actif (par exemple, avec les méthodes [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).

Si vous êtes en mode de mise à jour par lot, les enregistrements sont marqués pour suppression dans le cache et la suppression effective intervient lorsque vous appelez la méthode [UpdateBatch](updatebatch-method-ado.md). (Utilisez la propriété [Filter](filter-property-ado.md) pour consulter les enregistrements supprimés.)

Une tentative de récupération des valeurs des champs de l'enregistrement supprimé génère une erreur. Après la suppression de l'enregistrement actif, l'enregistrement supprimé reste actif jusqu'à ce que vous accédiez à un autre enregistrement. Dès que vous avez quitté l'enregistrement supprimé, ce dernier n'est plus accessible.

Si vous imbriquez des suppressions dans une transaction, vous pouvez récupérer des enregistrements supprimés avec la méthode [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). En mode de mise à jour par lot, vous pouvez annuler une suppression en attente ou un groupe de suppressions en attente avec la méthode [Cancel Batch](cancelbatch-method-ado.md).

Si la tentative de suppression des enregistrements échoue en raison d'un conflit avec les données sous-jacentes (par exemple, si un autre utilisateur a déjà supprimé un enregistrement), le fournisseur retourne des avertissements dans la collection [Errors](errors-collection-ado.md) sans pour autant interrompre l'exécution du programme. Une erreur d'exécution se produit uniquement en cas de conflits sur tous les enregistrements demandés.

Si la propriété dynamique [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) est définie et que l'objet **Recordset** résulte de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Delete** supprime uniquement les lignes de la table nommée dans la propriété [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

