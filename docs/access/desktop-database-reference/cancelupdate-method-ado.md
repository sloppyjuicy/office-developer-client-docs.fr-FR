---
title: CancelUpdate, méthode (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711244"
---
# <a name="cancelupdate-method-ado"></a>CancelUpdate, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Annule toutes les modifications apportées à la ligne active ou à une nouvelle ligne d'un objet [Recordset](recordset-object-ado.md) ou dans la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md) avant que la méthode [Update](update-method-ado.md) soit appelée.

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. CancelUpdate

*enregistrement*. *Champs*. CancelUpdate

## <a name="remarks"></a>Notes

**Objet Recordset**

Faites appel à la méthode **CancelUpdate** pour annuler les modifications apportées à la ligne active ou pour supprimer la ligne que vous venez d'ajouter. Vous ne pouvez pas effectuer ces opérations après avoir appelé la méthode **Update** sauf si ces modifications font partie d'une transaction que vous pouvez annuler à l'aide de la méthode [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) ou d'une mise à jour par lot. Dans ce dernier cas, vous pouvez annuler la méthode **Update** à l'aide de la méthode **CancelUpdate** ou [CancelBatch](cancelbatch-method-ado.md).

Si vous ajoutez une nouvelle ligne, lorsque vous appelez la méthode **CancelUpdate**, la ligne active représente celle qui était active avant l'appel de la méthode [AddNew](addnew-method-ado.md).

Si vous êtes en mode édition et que vous voulez quitter l'enregistrement actif (par exemple, en utilisant [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md)), vous pouvez faire appel à la méthode **CancelUpdate** pour annuler les modifications en attente. Cette opération est nécessaire si la mise à jour ne peut pas être publiée dans la source de données (par exemple, une tentative de suppression qui échoue suite à des violations de l'intégrité du référentiel laisse l'objet **Recordset** en mode édition après un appel de [Delete](delete-method-ado-recordset.md)).

**Objet Record**

La méthode **CancelUpdate** annule toute insertion ou suppression en attente d'objets [Field](field-object-ado.md), ainsi que les mises à jour en attente des champs existants et rétablit leurs valeurs d'origine. La propriété [Status](status-property-ado-recordset.md) de tous les champs de la collection **Fields** a la valeur **adFieldOK**.

