---
title: UpdateBatch, méthode (ADO)
TOCTitle: UpdateBatch Method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73400abe1298520aadb3f82a242a2e50872be0ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875748"
---
# <a name="updatebatch-method-ado"></a>UpdateBatch, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Écrit toutes les mises à jour par lot en attente sur le disque.

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. UpdateBatch*AffectRecords*

## <a name="parameters"></a>Paramètres

  - *AffectRecords*

  - Facultatif. Valeur [AffectEnum](affectenum.md) indiquant le nombre d'enregistrements affectés par la méthode **UpdateBatch**.

## <a name="remarks"></a>Notes

Utilisez la méthode **UpdateBatch** lorsque vous modifiez un objet **Recordset** en mode de mise à jour par lot pour transmettre toutes les modifications apportées à un objet **Recordset** dans la base de données sous-jacente.

Si l'objet **Recordset** prend en charge la mise à jour par lot, vous pouvez mettre localement en cache plusieurs modifications apportées à un ou plusieurs enregistrements, jusqu'à ce que vous appeliez la méthode **UpdateBatch**. Si vous modifiez l'enregistrement actif ou si vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode [Update](update-method-ado.md) pour enregistrer les modifications en attente apportées à l'enregistrement actif avant de transmettre les modifications par lot au fournisseur. Vous ne devez utiliser la mise à jour par lot qu'avec un curseur statique ou jeu de clés.


> [!NOTE]
> <P>[!REMARQUE] Si vous spécifiez <STRONG>adAffectGroup</STRONG> comme valeur de ce paramètre, une erreur est générée lorsqu'il n'y a pas d'enregistrement visible dans l'objet <STRONG>Recordset</STRONG> actif (par exemple, un filtre qui ne donne aucun enregistrement correspondant).</P>



Si la transmission des modifications échoue pour un ou tous les enregistrements en raison d’un conflit avec les données sous-jacentes (par exemple, un enregistrement déjà supprimé par un autre utilisateur), le fournisseur renvoie des avertissements dans la collection [Errors](errors-collection-ado.md) et une erreur d’exécution est générée. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) et [Status](status-property-ado-recordset.md) pour rechercher les enregistrements à l’origine de conflits.

Pour annuler les mises à jour par lot en attente, utilisez la méthode [CancelBatch](cancelbatch-method-ado.md).

Si les propriétés dynamiques [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et [Update Resync](update-resync-property-dynamic-ado.md) sont définies et que l'objet **Recordset** est le résultat de l'exécution d'une opération JOIN sur plusieurs tables, l'exécution de la méthode **UpdateBatch** est implicitement suivie par la méthode [Resync](resync-method-ado.md) en fonction des paramètres définis dans la propriété **Update Resync**.

L'ordre dans lequel les mises à jour individuelles d'un lot sont effectuées sur la source de données ne correspond pas forcément à celui de leur exécution dans l'objet **Recordset** local. L'ordre de mises à jour dépend du fournisseur. Ne l'oubliez pas lorsque vous codez des mises à jour associées entre elles, comme des contraintes de clé externe en cas d'insertion ou de mise à jour.

