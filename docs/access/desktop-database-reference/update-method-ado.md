---
title: Update, méthode (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7501f7607dbee558a67dd0e11d7f2498874f8870
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950229"
---
# <a name="update-method-ado"></a>Update, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Enregistre les modifications apportées à la ligne active d'un objet [Recordset](recordset-object-ado.md) ou à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md).

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. Mettre à jour des*champs de* *valeurs*

*enregistrement*. *Champs*. Mise à jour

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Fields* |Facultatif. Valeur de type **Variant** représentant un nom unique ou tableau de valeurs **Variant** représentant les noms ou positions ordinales des champs à modifier.|
|*Values* |Facultatif. Valeur de type **Variant** représentant une valeur unique ou un tableau de valeurs **Variant** représentant les valeurs du ou des champs du nouvel enregistrement.|

## <a name="remarks"></a>Notes

### <a name="recordset"></a>Recordset

Utilisez la méthode **Update** pour enregistrer les modifications apportées à l'enregistrement actif d'un objet **Recordset** depuis l'appel de la méthode [AddNew](addnew-method-ado.md) ou la modification des valeurs des champs d'un enregistrement existant. L'objet **Recordset** doit prendre en charge les mises à jour.

Pour définir des valeurs de champ, effectuez l'une des actions suivantes :

- Affectez des valeurs à la propriété [Value](field-object-ado.md) d'un objet [Field](value-property-ado.md) et appelez la méthode **Update**.

- Passez un nom de champ et une valeur comme arguments avec l'appel de **Update**.

- Passez un tableau de noms de champs et un tableau de valeurs avec l'appel de **Update**.

Lorsque vous utilisez des tableaux de champs et de valeurs, ces deux tableaux doivent contenir le même nombre d'éléments. De même, l'ordre des noms de champs doit correspondre à l'ordre des valeurs des champs. Si le nombre et l'ordre des champs et des valeurs ne correspondent pas, une erreur est générée.

Si l'objet **Recordset** prend en charge la mise à jour par lot, vous pouvez mettre en cache plusieurs modifications d'un ou plusieurs enregistrements jusqu'à ce que vous appeliez la méthode [UpdateBatch](updatebatch-method-ado.md). Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode **Update** pour enregistrer les modifications en attente apportées à l'enregistrement avant de transmettre les modifications mises en cache au fournisseur.

Si vous quittez l'enregistrement ajouté ou modifié avant d'appeler la méthode **Update**, ADO appelle automatiquement la méthode **Update** pour enregistrer les modifications. Vous devez appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) si vous souhaitez annuler les modifications apportées à l'enregistrement actif ou supprimer un enregistrement qui vient d'être ajouté.

L'enregistrement actif reste actif après avoir appelé la méthode **Update**.

### <a name="record"></a>Rappel

La méthode **Update** finalise les ajouts, suppressions et mises à jour des champs de la collection [Fields](fields-collection-ado.md) d'un objet **Record**.

Par exemple, les champs supprimés avec la méthode **Delete** sont marqués immédiatement pour suppression mais restent dans la collection. La méthode **Update** doit être appelée pour supprimer réellement ces champs de la collection du fournisseur.

